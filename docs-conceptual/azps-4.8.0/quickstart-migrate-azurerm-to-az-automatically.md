---
title: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul
description: Hier finden Sie Informationen zur automatischen Migration von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427020"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="68074-103">Schnellstart: Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul</span><span class="sxs-lookup"><span data-stu-id="68074-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="68074-104">In diesem Artikel erfahren Sie, wie Sie das PowerShell-Modul „Az.Tools.Migration“ verwenden, um Ihre PowerShell-Skripts und Skriptmodule automatisch von AzureRM auf das Az PowerShell-Modul zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="68074-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68074-105">Das PowerShell Modul „Az.Tools.Migration“ befindet sich derzeit in der Public Preview-Phase.</span><span class="sxs-lookup"><span data-stu-id="68074-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="68074-106">Diese Vorschauversion wird ohne Vereinbarung zum Servicelevel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="68074-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="68074-107">Für Produktionsworkloads wird sie nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="68074-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="68074-108">Manche Features werden möglicherweise nicht unterstützt oder sind nur eingeschränkt verwendbar.</span><span class="sxs-lookup"><span data-stu-id="68074-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="68074-109">Weitere Informationen finden Sie unter [Zusätzliche Nutzungsbestimmungen für Microsoft Azure-Vorschauen](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="68074-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="68074-110">Wenn Sie Feedback geben oder Probleme im Zusammenhang mit dem PowerShell-Modul „Az.Tools.Migration“ melden möchten, können Sie [ein GitHub-Problem](https://github.com/Azure/azure-powershell-migration/issues) im Repository `azure-powershell-migration` erstellen.</span><span class="sxs-lookup"><span data-stu-id="68074-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="68074-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="68074-111">Requirements</span></span>

* <span data-ttu-id="68074-112">Aktualisieren Sie Ihre vorhandenen PowerShell-Skripts auf die [aktuelle Version des AzureRM PowerShell-Moduls (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="68074-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="68074-113">Installieren Sie das PowerShell-Modul „Az.Tools.Migration“.</span><span class="sxs-lookup"><span data-stu-id="68074-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="68074-114">Schritt 1: Generieren eines Upgradeplans</span><span class="sxs-lookup"><span data-stu-id="68074-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="68074-115">Verwenden Sie das Cmdlet `New-AzUpgradeModulePlan`, um einen Upgradeplan für die Migration Ihrer Skripts und Module zum Az PowerShell-Modul zu generieren.</span><span class="sxs-lookup"><span data-stu-id="68074-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="68074-116">Der Upgradeplan enthält die spezifische Datei sowie die Punkte, die Änderungen erfordern, wenn Sie von AzureRM auf die Az PowerShell-Cmdlets umstellen.</span><span class="sxs-lookup"><span data-stu-id="68074-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="68074-117">Durch das Cmdlet `New-AzUpgradeModulePlan` wird der Plan nicht ausgeführt. Es werden lediglich die Upgradeschritte generiert.</span><span class="sxs-lookup"><span data-stu-id="68074-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="68074-118">Überprüfen Sie die Ergebnisse des Upgradeplans.</span><span class="sxs-lookup"><span data-stu-id="68074-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="68074-119">Führen Sie den folgenden Befehl aus, um die Ergebnisse nach Befehlen zu filtern, für die Warnungen oder Fehler vorliegen.</span><span class="sxs-lookup"><span data-stu-id="68074-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="68074-120">Dies kann bei umfangreichen Resultsets hilfreich sein, um Fehler vor der Durchführung des Upgrades schnell zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="68074-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="68074-121">Schritt 2: Durchführen des Upgrades</span><span class="sxs-lookup"><span data-stu-id="68074-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="68074-122">Der Upgradeplan wird ausgeführt, wenn Sie das Cmdlet `Invoke-AzUpgradeModulePlan` ausführen.</span><span class="sxs-lookup"><span data-stu-id="68074-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="68074-123">Durch diesen Befehl wird ein Upgrade für die angegebene Datei oder die angegebenen Ordner durchgeführt (ausgenommen bei Fehlern, die ggf. durch das Cmdlet `New-AzUpgradeModulePlan` identifiziert wurden).</span><span class="sxs-lookup"><span data-stu-id="68074-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="68074-124">Bei diesem Befehl müssen Sie angeben, ob die Dateien direkt geändert werden sollen oder ob parallel zu den ursprünglichen Dateien neue Dateien gespeichert werden sollen, sodass die Originaldateien erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="68074-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="68074-125">Der Vorgang kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="68074-125">There is no undo operation.</span></span> <span data-ttu-id="68074-126">Achten Sie immer darauf, dass Sie über eine Sicherungskopie der PowerShell-Skripts und -Module verfügen, für die Sie ein Upgrade durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="68074-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="68074-127">Bei Angabe der Option `-FileEditMode ModifyExistingFiles` ist das Cmdlet `Invoke-AzUpgradeModulePlan` destruktiv.</span><span class="sxs-lookup"><span data-stu-id="68074-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="68074-128">Ihre Skripts und Funktionen werden in diesem Fall direkt gemäß dem Modulupgradeplan geändert, der durch das Cmdlet `New-AzUpgradeModulePlan` generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="68074-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="68074-129">Alternativ können Sie die nicht destruktive Option `-FileEditMode SaveChangesToNewFiles` angeben.</span><span class="sxs-lookup"><span data-stu-id="68074-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="68074-130">Überprüfen Sie die Ergebnisse des Upgradevorgangs.</span><span class="sxs-lookup"><span data-stu-id="68074-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="68074-131">Sollten Fehler zurückgegeben werden, können Sie sich die Fehlerergebnisse mithilfe des folgenden Befehls genauer ansehen:</span><span class="sxs-lookup"><span data-stu-id="68074-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="68074-132">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="68074-132">Limitations</span></span>

* <span data-ttu-id="68074-133">Automatisierte Parameternamenaktualisierungen werden für Parametersätze mit Splatting nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68074-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="68074-134">Falls während der Generierung des Upgradeplans welche gefunden werden, wird eine Warnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68074-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="68074-135">Bei Datei-E/A-Vorgängen wird die Standardcodierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="68074-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="68074-136">Ungewöhnliche Dateicodierungen können zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="68074-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="68074-137">AzureRM-Cmdlets, die als Argumente an simulierte Anweisungen für Pester-Komponententests übergeben werden, werden nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="68074-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="68074-138">Aktuell wird nur die Version 4.6.1 des Az PowerShell-Moduls als Ziel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68074-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="68074-139">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="68074-139">Next steps</span></span>

<span data-ttu-id="68074-140">Weitere Informationen zum Az PowerShell-Modul finden Sie in der [Azure PowerShell-Dokumentation](/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="68074-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>