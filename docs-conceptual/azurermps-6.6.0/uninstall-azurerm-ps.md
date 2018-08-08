---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 92af0fdd8db451e2f0f092d66a3e296ad8d6a09e
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368210"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="cd090-103">Deinstallieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="cd090-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="cd090-104">In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen.</span><span class="sxs-lookup"><span data-stu-id="cd090-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="cd090-105">Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cd090-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="cd090-106">Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="cd090-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi"></a><span data-ttu-id="cd090-107">Deinstallieren einer MSI</span><span class="sxs-lookup"><span data-stu-id="cd090-107">Uninstall MSI</span></span>

<span data-ttu-id="cd090-108">Falls Sie Azure PowerShell mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd090-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="cd090-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="cd090-109">Platform</span></span> | <span data-ttu-id="cd090-110">Anleitung</span><span class="sxs-lookup"><span data-stu-id="cd090-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="cd090-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd090-111">Windows 10</span></span> | <span data-ttu-id="cd090-112">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="cd090-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="cd090-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd090-113">Windows 7</span></span> </br><span data-ttu-id="cd090-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd090-114">Windows 8</span></span> | <span data-ttu-id="cd090-115">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="cd090-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="cd090-116">Auf diesem Bildschirm sollte „Azure PowerShell“ in der Programmliste aufgeführt sein. Sie können die Anwendung dort deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="cd090-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="cd090-117">Deinstallieren über PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd090-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="cd090-118">Falls Sie Azure PowerShell mithilfe von PowerShellGet installiert haben, können Sie das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module) verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd090-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="cd090-119">Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="cd090-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="cd090-120">Wenn Sie Azure PowerShell vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="cd090-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="cd090-121">Die Deinstallation kann kompliziert sein, wenn mehrere Versionen von Azure PowerShell installiert sind.</span><span class="sxs-lookup"><span data-stu-id="cd090-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="cd090-122">Das folgende Skript kann verwendet werden, um eine einzelne Version von Azure PowerShell vollständig zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="cd090-122">The following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="cd090-123">Das Skript fragt den PowerShell-Katalog ab, um eine Liste der abhängigen Submodule abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cd090-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="cd090-124">Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="cd090-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="cd090-125">Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="cd090-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="cd090-126">Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version von Azure PowerShell zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="cd090-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="cd090-127">Bei der Ausführung des Skripts werden jeweils der Name und die Version des Submoduls angezeigt, das gerade deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="cd090-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="cd090-128">Führen Sie diesen Befehl für jede Azure PowerShell-Version aus, die Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cd090-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>