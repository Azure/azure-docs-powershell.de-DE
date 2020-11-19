---
title: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul
description: Hier finden Sie Informationen zur automatischen Migration von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715547"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Schnellstart: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul

In diesem Artikel erfahren Sie, wie Sie das PowerShell-Modul „Az.Tools.Migration“ verwenden, um Ihre PowerShell-Skripts und Skriptmodule automatisch von AzureRM auf das Az PowerShell-Modul zu aktualisieren.

> [!IMPORTANT]
> Das PowerShell Modul „Az.Tools.Migration“ befindet sich derzeit in der Public Preview-Phase. Diese Vorschauversion wird ohne Vereinbarung zum Servicelevel bereitgestellt. Für Produktionsworkloads wird sie nicht empfohlen. Manche Features werden möglicherweise nicht unterstützt oder sind nur eingeschränkt verwendbar. Weitere Informationen finden Sie unter [Zusätzliche Nutzungsbestimmungen für Microsoft Azure-Vorschauen](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Wenn Sie Feedback geben oder Probleme im Zusammenhang mit dem PowerShell-Modul „Az.Tools.Migration“ melden möchten, können Sie [ein GitHub-Problem](https://github.com/Azure/azure-powershell-migration/issues) im Repository `azure-powershell-migration` erstellen.

## <a name="requirements"></a>Requirements (Anforderungen)

* Aktualisieren Sie Ihre vorhandenen PowerShell-Skripts auf die [aktuelle Version des AzureRM PowerShell-Moduls (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Installieren Sie das PowerShell-Modul „Az.Tools.Migration“.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Schritt 1: Generieren eines Upgradeplans

Verwenden Sie das Cmdlet `New-AzUpgradeModulePlan`, um einen Upgradeplan für die Migration Ihrer Skripts und Module zum Az PowerShell-Modul zu generieren. Der Upgradeplan enthält die spezifische Datei sowie die Punkte, die Änderungen erfordern, wenn Sie von AzureRM auf die Az PowerShell-Cmdlets umstellen.

> [!NOTE]
> Durch das Cmdlet `New-AzUpgradeModulePlan` wird der Plan nicht ausgeführt. Es werden lediglich die Upgradeschritte generiert.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Überprüfen Sie die Ergebnisse des Upgradeplans.

```powershell
# Show the entire upgrade plan
$Plan
```

Führen Sie den folgenden Befehl aus, um die Ergebnisse nach Befehlen zu filtern, für die Warnungen oder Fehler vorliegen. Dies kann bei umfangreichen Resultsets hilfreich sein, um Fehler vor der Durchführung des Upgrades schnell zu identifizieren.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>Schritt 2: Durchführen des Upgrades

Der Upgradeplan wird ausgeführt, wenn Sie das Cmdlet `Invoke-AzUpgradeModulePlan` ausführen. Durch diesen Befehl wird ein Upgrade für die angegebene Datei oder die angegebenen Ordner durchgeführt (ausgenommen bei Fehlern, die ggf. durch das Cmdlet `New-AzUpgradeModulePlan` identifiziert wurden).

Bei diesem Befehl müssen Sie angeben, ob die Dateien direkt geändert werden sollen oder ob parallel zu den ursprünglichen Dateien neue Dateien gespeichert werden sollen, sodass die Originaldateien erhalten bleiben.

> [!CAUTION]
> Der Vorgang kann nicht rückgängig gemacht werden. Achten Sie immer darauf, dass Sie über eine Sicherungskopie der PowerShell-Skripts und -Module verfügen, für die Sie ein Upgrade durchführen möchten.

> [!WARNING]
> Bei Angabe der Option `-FileEditMode ModifyExistingFiles` ist das Cmdlet `Invoke-AzUpgradeModulePlan` destruktiv. Ihre Skripts und Funktionen werden in diesem Fall direkt gemäß dem Modulupgradeplan geändert, der durch das Cmdlet `New-AzUpgradeModulePlan` generiert wurde. Alternativ können Sie die nicht destruktive Option `-FileEditMode SaveChangesToNewFiles` angeben.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Überprüfen Sie die Ergebnisse des Upgradevorgangs.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Sollten Fehler zurückgegeben werden, können Sie sich die Fehlerergebnisse mithilfe des folgenden Befehls genauer ansehen:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Einschränkungen

* Automatisierte Parameternamenaktualisierungen werden für Parametersätze mit Splatting nicht unterstützt. Falls während der Generierung des Upgradeplans welche gefunden werden, wird eine Warnung zurückgegeben.
* Bei Datei-E/A-Vorgängen wird die Standardcodierung verwendet. Ungewöhnliche Dateicodierungen können zu Problemen führen.
* AzureRM-Cmdlets, die als Argumente an simulierte Anweisungen für Pester-Komponententests übergeben werden, werden nicht erkannt.
* Aktuell wird nur die Version 4.6.1 des Az PowerShell-Moduls als Ziel unterstützt.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zum Az PowerShell-Modul finden Sie in der [Azure PowerShell-Dokumentation](https://docs.microsoft.com/powershell/azure/).