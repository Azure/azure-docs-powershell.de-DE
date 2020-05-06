---
title: Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen
description: Hier erfahren Sie, wie Sie Azure PowerShell-Cmdlets mithilfe von „-AsJob“ und „Start-Job“ parallel oder als Hintergrundaufgaben ausführen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "81740489"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen

Da von Azure PowerShell eine Verbindung mit einer Azure-Cloud hergestellt und auf Antworten gewartet werden muss, wird Ihre PowerShell-Sitzung durch die meisten dieser Cmdlets blockiert, bis eine Antwort von der Cloud empfangen wird.
Mithilfe von PowerShell-Aufträgen können Sie Cmdlets im Hintergrund ausführen oder gleichzeitig mehrere Azure-Aufgaben in einer einzelnen PowerShell-Sitzung erledigen.

Dieser Artikel enthält eine kurze Übersicht über das Ausführen von Azure PowerShell-Cmdlets als PowerShell-Aufträge sowie über das Überprüfen des Abschlusses. Wenn Sie Befehle in Azure PowerShell ausführen möchten, müssen Sie Azure PowerShell-Kontexte verwenden. Diese werden unter [Azure-Kontexte und -Anmeldeinformationen](context-persistence.md) ausführlich behandelt.
Weitere Informationen zu PowerShell-Aufträgen finden Sie unter [Informationen zu Aufträgen](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Azure-Kontexte mit PowerShell-Aufträgen

Da PowerShell-Aufträge als separate Prozesse ohne angefügte PowerShell-Sitzung ausgeführt werden, müssen Ihre Azure-Anmeldeinformationen an sie weitergegeben werden. Anmeldeinformationen werden mithilfe einer der folgenden Methoden als Azure-Kontextobjekte übergeben:

* Automatische Kontextpersistenz: Die Kontextpersistenz ist standardmäßig aktiviert und behält Ihre Anmeldeinformationen über mehrere Sitzungen hinweg bei. Bei aktivierter Kontextpersistenz wird der aktuelle Azure-Kontext an den neuen Prozess übergeben:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Verwendung des Parameters `-AzContext` mit beliebigen Azure PowerShell-Cmdlets, um ein Azure-Kontextobjekt bereitzustellen:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Bei deaktivierter Kontextpersistenz wird das Argument `-AzContext` benötigt.

* Verwendung des Schalters `-AsJob`, der von einigen Azure PowerShell-Cmdlets bereitgestellt wird. Dieser Schalter startet das Cmdlet automatisch als PowerShell-Auftrag und verwendet dabei den derzeit aktiven Azure-Kontext:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Ob ein Cmdlet `-AsJob` unterstützt, erfahren Sie in der zugehörigen Referenzdokumentation. Für den Schalter `-AsJob` muss die automatische Kontextspeicherung nicht aktiviert sein.

Der Status eines aktiven Auftrags kann mithilfe des Cmdlets [Get-Job](/powershell/module/microsoft.powershell.core/get-job) überprüft werden. Wenn Sie die bisherige Ausgabe eines Auftrags abrufen möchten, verwenden Sie das Cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Wenn Sie den Fortschritt eines Vorgangs remote in Azure überprüfen möchten, verwenden Sie die Cmdlets vom Typ `Get-` für die Art der Ressource, die durch den Auftrag geändert wird:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Weitere Informationen

* [Azure PowerShell-Kontextobjekte](context-persistence.md)
* [Informationen zu Aufträgen](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
