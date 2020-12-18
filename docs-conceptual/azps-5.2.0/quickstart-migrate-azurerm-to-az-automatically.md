---
title: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul
description: Hier finden Sie Informationen zur automatischen Migration von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488528"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Schnellstart: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul

In diesem Artikel erfahren Sie, wie Sie das PowerShell-Modul „Az.Tools.Migration“ verwenden, um Ihre PowerShell-Skripts und Skriptmodule automatisch von AzureRM auf das Az PowerShell-Modul zu aktualisieren.

> [!IMPORTANT]
> Das PowerShell Modul „Az.Tools.Migration“ befindet sich derzeit in der Public Preview-Phase. Diese Vorschauversion wird ohne Vereinbarung zum Servicelevel bereitgestellt. Für Produktionsworkloads wird sie nicht empfohlen. Manche Features werden möglicherweise nicht unterstützt oder sind nur eingeschränkt verwendbar. Weitere Informationen finden Sie unter [Zusätzliche Nutzungsbestimmungen für Microsoft Azure-Vorschauen](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

## <a name="requirements"></a>Requirements (Anforderungen)

* Aktualisieren Sie Ihre vorhandenen PowerShell-Skripts auf die [aktuelle Version des AzureRM PowerShell-Moduls (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Installieren Sie das PowerShell-Modul „Az.Tools.Migration“.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Schritt 1: Generieren eines Upgradeplans

Verwenden Sie das Cmdlet **`New-AzUpgradeModulePlan`** , um einen Upgradeplan für die Migration Ihrer Skripts und Module zum Az PowerShell-Modul zu generieren. Dieses Cmdlet nimmt keine Änderungen an Ihren vorhandenen Skripts vor. Verwenden Sie den Parameter **`FilePath`** für ein bestimmtes Skript oder den Parameter **`DirectoryPath`** für alle Skripts in einem bestimmten Ordner.

> [!NOTE]
> Durch das Cmdlet **`New-AzUpgradeModulePlan`** wird der Plan nicht ausgeführt. Es werden lediglich die Upgradeschritte generiert.

Im folgenden Beispiel wird ein Plan für alle Skripts im Ordner _`C:\Scripts`_ generiert. Der Parameter **`OutVariable`** wird angegeben, sodass die Ergebnisse zurückgegeben und gleichzeitig in einer Variablen mit dem Namen **`Plan`** gespeichert werden.

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Wie in der folgenden Ausgabe gezeigt, enthält der Upgradeplan die spezifische Datei sowie die Punkte, die Änderungen erfordern, wenn Sie von AzureRM auf die Az PowerShell-Cmdlets umstellen.

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

Vor der Durchführung des Upgrades müssen Sie die Ergebnisse des Plans auf Probleme überprüfen. Im folgenden Beispiel wird eine Liste der Skripts und der Elemente in diesen Skripts zurückgegeben, die das automatische Upgrade verhindern.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

Die in der folgenden Ausgabe angezeigten Elemente werden erst dann automatisch aktualisiert, wenn die Probleme manuell behoben wurden. Zu bekannten Problemen, die eine automatische Aktualisierung verhindern, zählen Befehle, die Splatting verwenden.

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a>Schritt 2: Durchführen des Upgrades

> [!CAUTION]
> Der Vorgang kann nicht rückgängig gemacht werden. Achten Sie immer darauf, dass Sie über eine Sicherungskopie der PowerShell-Skripts und -Module verfügen, für die Sie ein Upgrade durchführen möchten.

Wenn Sie mit dem Plan zufrieden sind, wird das Upgrade mit dem Cmdlet **`Invoke-AzUpgradeModulePlan`** durchgeführt. Geben Sie **`SaveChangesToNewFiles`** für den Parameterwert **`FileEditMode`** an, um zu verhindern, dass Änderungen an den ursprünglichen Skripts vorgenommen werden. Bei Verwendung dieses Modus wird das Upgrade durchgeführt, indem eine Kopie jedes Skripts erstellt und an die Dateinamen jeweils _`_az_upgraded`_ angefügt wird.

> [!WARNING]
> Bei Angabe der Option **`-FileEditMode ModifyExistingFiles`** ist das Cmdlet **`Invoke-AzUpgradeModulePlan`** destruktiv. Ihre Skripts und Funktionen werden in diesem Fall direkt gemäß dem Modulupgradeplan geändert, der durch das Cmdlet **`New-AzUpgradeModulePlan`** generiert wurde. Alternativ können Sie die nicht destruktive Option **`-FileEditMode SaveChangesToNewFiles`** angeben.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

Sollten Fehler zurückgegeben werden, können Sie sich die Fehlerergebnisse mithilfe des folgenden Befehls genauer ansehen:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a>Einschränkungen

* Automatisierte Parameternamenaktualisierungen werden für Parametersätze mit Splatting nicht unterstützt. Falls während der Generierung des Upgradeplans welche gefunden werden, wird eine Warnung zurückgegeben.
* Bei Datei-E/A-Vorgängen wird die Standardcodierung verwendet. Ungewöhnliche Dateicodierungen können zu Problemen führen.
* AzureRM-Cmdlets, die als Argumente an simulierte Anweisungen für Pester-Komponententests übergeben werden, werden nicht erkannt.
* Aktuell wird nur die Version 4.6.1 des Az PowerShell-Moduls als Ziel unterstützt.

## <a name="how-to-report-issues"></a>Melden von Problemen

Wenn Sie Feedback geben oder Probleme im Zusammenhang mit dem PowerShell-Modul „Az.Tools.Migration“ melden möchten, können Sie [ein GitHub-Problem](https://github.com/Azure/azure-powershell-migration/issues) im Repository `azure-powershell-migration` erstellen.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zum Az PowerShell-Modul finden Sie in der [Azure PowerShell-Dokumentation](/powershell/azure/).