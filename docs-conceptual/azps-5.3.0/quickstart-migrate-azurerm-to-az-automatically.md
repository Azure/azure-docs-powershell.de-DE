---
title: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul
description: Hier finden Sie Informationen zur automatischen Migration von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893788"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="c13f7-103">Schnellstart: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul</span><span class="sxs-lookup"><span data-stu-id="c13f7-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="c13f7-104">In diesem Artikel erfahren Sie, wie Sie das PowerShell-Modul „Az.Tools.Migration“ verwenden, um Ihre PowerShell-Skripts und Skriptmodule automatisch von AzureRM auf das Az PowerShell-Modul zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c13f7-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="c13f7-105">Weitere Migrationsoptionen finden Sie unter [Migrieren von Azure PowerShell von AzureRM zum Az-Modul](/powershell/azure/migrate-from-azurerm-to-az).</span><span class="sxs-lookup"><span data-stu-id="c13f7-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="c13f7-106">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c13f7-106">Requirements</span></span>

* <span data-ttu-id="c13f7-107">Aktualisieren Sie Ihre vorhandenen PowerShell-Skripts auf die [aktuelle Version des AzureRM PowerShell-Moduls (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="c13f7-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="c13f7-108">Installieren Sie das PowerShell-Modul „Az.Tools.Migration“.</span><span class="sxs-lookup"><span data-stu-id="c13f7-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="c13f7-109">Schritt 1: Generieren eines Upgradeplans</span><span class="sxs-lookup"><span data-stu-id="c13f7-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="c13f7-110">Verwenden Sie das Cmdlet **`New-AzUpgradeModulePlan`** , um einen Upgradeplan für die Migration Ihrer Skripts und Module zum Az PowerShell-Modul zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c13f7-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="c13f7-111">Dieses Cmdlet nimmt keine Änderungen an Ihren vorhandenen Skripts vor.</span><span class="sxs-lookup"><span data-stu-id="c13f7-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="c13f7-112">Verwenden Sie den Parameter **`FilePath`** für ein bestimmtes Skript oder den Parameter **`DirectoryPath`** für alle Skripts in einem bestimmten Ordner.</span><span class="sxs-lookup"><span data-stu-id="c13f7-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="c13f7-113">Durch das Cmdlet **`New-AzUpgradeModulePlan`** wird der Plan nicht ausgeführt. Es werden lediglich die Upgradeschritte generiert.</span><span class="sxs-lookup"><span data-stu-id="c13f7-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="c13f7-114">Im folgenden Beispiel wird ein Plan für alle Skripts im Ordner _`C:\Scripts`_ generiert.</span><span class="sxs-lookup"><span data-stu-id="c13f7-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="c13f7-115">Der Parameter **`OutVariable`** wird angegeben, sodass die Ergebnisse zurückgegeben und gleichzeitig in einer Variablen mit dem Namen **`Plan`** gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c13f7-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="c13f7-116">Wie in der folgenden Ausgabe gezeigt, enthält der Upgradeplan die spezifische Datei sowie die Punkte, die Änderungen erfordern, wenn Sie von AzureRM auf die Az PowerShell-Cmdlets umstellen.</span><span class="sxs-lookup"><span data-stu-id="c13f7-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

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

<span data-ttu-id="c13f7-117">Vor der Durchführung des Upgrades müssen Sie die Ergebnisse des Plans auf Probleme überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c13f7-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="c13f7-118">Im folgenden Beispiel wird eine Liste der Skripts und der Elemente in diesen Skripts zurückgegeben, die das automatische Upgrade verhindern.</span><span class="sxs-lookup"><span data-stu-id="c13f7-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="c13f7-119">Die in der folgenden Ausgabe angezeigten Elemente werden erst dann automatisch aktualisiert, wenn die Probleme manuell behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="c13f7-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span>

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

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="c13f7-120">Schritt 2: Durchführen des Upgrades</span><span class="sxs-lookup"><span data-stu-id="c13f7-120">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="c13f7-121">Der Vorgang kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="c13f7-121">There is no undo operation.</span></span> <span data-ttu-id="c13f7-122">Achten Sie immer darauf, dass Sie über eine Sicherungskopie der PowerShell-Skripts und -Module verfügen, für die Sie ein Upgrade durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="c13f7-122">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="c13f7-123">Wenn Sie mit dem Plan zufrieden sind, wird das Upgrade mit dem Cmdlet **`Invoke-AzUpgradeModulePlan`** durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c13f7-123">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="c13f7-124">Geben Sie **`SaveChangesToNewFiles`** für den Parameterwert **`FileEditMode`** an, um zu verhindern, dass Änderungen an den ursprünglichen Skripts vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c13f7-124">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="c13f7-125">Bei Verwendung dieses Modus wird das Upgrade durchgeführt, indem eine Kopie jedes Skripts erstellt und an die Dateinamen jeweils _`_az_upgraded`_ angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c13f7-125">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="c13f7-126">Bei Angabe der Option **`-FileEditMode ModifyExistingFiles`** ist das Cmdlet **`Invoke-AzUpgradeModulePlan`** destruktiv.</span><span class="sxs-lookup"><span data-stu-id="c13f7-126">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="c13f7-127">Ihre Skripts und Funktionen werden in diesem Fall direkt gemäß dem Modulupgradeplan geändert, der durch das Cmdlet **`New-AzUpgradeModulePlan`** generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c13f7-127">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="c13f7-128">Alternativ können Sie die nicht destruktive Option **`-FileEditMode SaveChangesToNewFiles`** angeben.</span><span class="sxs-lookup"><span data-stu-id="c13f7-128">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

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

<span data-ttu-id="c13f7-129">Sollten Fehler zurückgegeben werden, können Sie sich die Fehlerergebnisse mithilfe des folgenden Befehls genauer ansehen:</span><span class="sxs-lookup"><span data-stu-id="c13f7-129">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

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

## <a name="limitations"></a><span data-ttu-id="c13f7-130">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c13f7-130">Limitations</span></span>

* <span data-ttu-id="c13f7-131">Bei Datei-E/A-Vorgängen wird die Standardcodierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c13f7-131">File I/O operations use default encoding.</span></span> <span data-ttu-id="c13f7-132">Ungewöhnliche Dateicodierungen können zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="c13f7-132">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="c13f7-133">AzureRM-Cmdlets, die als Argumente an simulierte Anweisungen für Pester-Komponententests übergeben werden, werden nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="c13f7-133">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="c13f7-134">Aktuell wird nur die Version 5.2.0 des Az PowerShell-Moduls als Ziel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c13f7-134">Currently, only Az PowerShell module version 5.2.0 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="c13f7-135">Melden von Problemen</span><span class="sxs-lookup"><span data-stu-id="c13f7-135">How to report issues</span></span>

<span data-ttu-id="c13f7-136">Wenn Sie Feedback geben oder Probleme im Zusammenhang mit dem PowerShell-Modul „Az.Tools.Migration“ melden möchten, können Sie [ein GitHub-Problem](https://github.com/Azure/azure-powershell-migration/issues) im Repository `azure-powershell-migration` erstellen.</span><span class="sxs-lookup"><span data-stu-id="c13f7-136">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c13f7-137">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c13f7-137">Next steps</span></span>

<span data-ttu-id="c13f7-138">Weitere Informationen zum Az PowerShell-Modul finden Sie in der [Azure PowerShell-Dokumentation](/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="c13f7-138">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
