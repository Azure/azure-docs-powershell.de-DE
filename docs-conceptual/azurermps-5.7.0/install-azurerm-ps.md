---
title: Installieren von Azure PowerShell unter Windows mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: c0bb020fc8cc77b96dc7fe6839911a4d80974d9e
ms.sourcegitcommit: f08f501b75a97ceef59c21f42158bf135a354eaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2018
ms.locfileid: "37926245"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installieren von Azure PowerShell unter Windows mit PowerShellGet

In diesem Artikel erfahren Sie, wie Sie die Azure PowerShell-Module in einer Windows-Umgebung unter Verwendung von PowerShellGet installieren. PowerShellGet und die Modulverwaltung stellen die bevorzugte Installationsmethode für Azure PowerShell dar. Sie können aber auch den Webplattform-Installer oder das MSI-Paket verwenden. Entsprechende Informationen finden Sie unter [Andere Installationsmethoden](other-install.md).

Eine Anleitung zum Installieren von Azure PowerShell auf anderen Plattformen finden Sie unter [Installieren und Konfigurieren von Azure PowerShell unter macOS und Linux](install-azurermps-maclinux.md).

Das klassische Azure-Bereitstellungsmodell wird von dieser Version von Azure PowerShell nicht unterstützt. Befolgen Sie die Anleitung unter [Installieren des Azure PowerShell-Dienstverwaltungsmoduls](/powershell/azure/servicemanagement/install-azure-ps), um Unterstützung zu klassischen Bereitstellungen zu erhalten.

## <a name="requirements"></a>Requirements (Anforderungen)

Für die Installation von Azure PowerShell benötigen Sie PowerShellGet Version 1.1.2.0 oder höher. Führen Sie den folgenden Befehl aus, um zu prüfen, ob diese Version unter Ihrem System verfügbar ist:

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Etwa folgende Ausgabe sollte angezeigt werden:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Führen Sie den folgenden Befehl aus, wenn Sie Ihre Installation von PowerShellGet aktualisieren müssen:

```powershell
Install-Module PowerShellGet -Force
```

Befolgen Sie die Anleitung unten in der Tabelle, falls Sie PowerShellGet nicht installiert haben.

|Szenario|Installationsanleitung|
|---|---|
|Windows 10<br/>Windows Server 2016|In Windows Management Framework (WMF) 5.0 integriert (im Betriebssystem enthalten)|
|Upgrade auf PowerShell 5| <ol><li>[Installieren Sie die aktuelle Version von WMF.](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Führen Sie den folgenden Befehl aus:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows mit PowerShell 3 oder PowerShell 4|<ol><il>[Laden Sie die PackageManagement-Module herunter.](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Führen Sie den folgenden Befehl aus:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> Für die Verwendung von PowerShellGet ist eine Ausführungsrichtlinie erforderlich, die die Ausführung von Skripts ermöglicht. Weitere Informationen zur Ausführungsrichtlinie von PowerShell finden Sie unter [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informationen zu Ausführungsrichtlinien).

> [!IMPORTANT]
> Das in diesem Dokument beschriebene Modul „AzureRM“ verwendet .NET Framework. Dadurch ist es nicht mit PowerShell 6.0 kompatibel, das .NET Core verwendet. Wenn Sie PowerShell 6.0 verwenden, befolgen Sie die [Installationsanweisungen für macOS und Linux](install-azurermps-maclinux.md). 

## <a name="install-the-azure-powershell-module"></a>Installieren des Azure PowerShell-Moduls

Sie benötigen erhöhte Rechte, um Module aus dem PowerShell-Katalog installieren zu können. Führen Sie den folgenden Befehl in einer Sitzung mit erhöhten Rechten aus, um Azure PowerShell zu installieren:

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> Wenn Sie eine ältere NuGet-Version als 2.8.5.201 haben, werden Sie aufgefordert, die aktuelle NuGet-Version herunterzuladen und zu installieren.

Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert. Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.

Das Modul `AzureRM` ist ein Rollupmodul für die Azure PowerShell-Cmdlets. Wenn Sie es installieren, werden alle verfügbaren Azure Resource Manager-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.

## <a name="sign-in"></a>Anmelden

Damit Sie Azure PowerShell verwenden können, müssen Sie `AzureRM` mit dem [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module)-Cmdlet in Ihre aktuelle PowerShell-Sitzung laden und sich dann mit Ihren Azure-Anmeldeinformationen anmelden.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Für den automatischen Import des Moduls `AzureRM` muss ein PowerShell-Profil eingerichtet werden. Informationen hierzu finden Sie unter [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles) (Informationen zu Profilen).
Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung finden Sie unter [Persisting user credentials across PowerShell sessions](context-persistence.md) (Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen).

## <a name="update-the-azure-powershell-module"></a>Aktualisieren des Azure PowerShell-Moduls

Sie können Ihre Azure PowerShell-Installation aktualisieren, indem Sie [Update-Module](/powershell/module/powershellget/update-module) ausführen. Mit diesem Befehl werden __keine__ früheren Versionen deinstalliert.

```powershell
Update-Module -Name AzureRM
```

Wenn Sie ältere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md) (Deinstallieren des Azure PowerShell-Moduls) weiter.

## <a name="use-multiple-versions-of-azure-powershell"></a>Verwenden von mehreren Versionen von Azure PowerShell

Es ist möglich, mehrere Versionen von Azure PowerShell zu installieren. Unter Umständen benötigen Sie mehr als eine Version, wenn Sie mit lokalen Azure Stack-Ressourcen arbeiten, eine ältere Version von Windows ausführen, die nicht auf PowerShell 5.0 aktualisiert werden kann, oder das klassische Azure-Bereitstellungsmodell nutzen. Geben Sie beim Installieren das Argument `-RequiredVersion` an, um eine ältere Version zu installieren.

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Beim Laden des Azure PowerShell-Moduls wird standardmäßig die aktuelle Version geladen. Geben Sie das Argument `-RequiredVersion` an, um eine andere Version zu laden.

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a>Feedback geben

Bitte [melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie bei der Nutzung von Azure PowerShell einen Fehler finden.
Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zum Modul und zu den zugehörigen Features als Einstieg in die Nutzung von Azure PowerShell finden Sie unter [Get started with Azure PowerShell](get-started-azureps.md) (Erste Schritte mit Azure PowerShell).