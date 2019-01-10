---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 9d1f1b6550c39b8c65662cf0150f477392747708
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594792"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="f6430-103">Deinstallieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="f6430-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="f6430-104">In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen.</span><span class="sxs-lookup"><span data-stu-id="f6430-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="f6430-105">Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f6430-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="f6430-106">Sollte ein Fehler auftreten, können Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="f6430-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="f6430-107">Deinstallieren des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="f6430-107">Uninstall the Az module</span></span>

<span data-ttu-id="f6430-108">Verwenden Sie zum Deinstallieren der Az-Module das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="f6430-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="f6430-109">Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="f6430-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="f6430-110">Wenn Sie Azure PowerShell vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="f6430-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="f6430-111">Die Deinstallation kann kompliziert sein, wenn Sie mehrere Versionen von Azure PowerShell installiert haben.</span><span class="sxs-lookup"><span data-stu-id="f6430-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="f6430-112">Überprüfen Sie mit dem folgenden Befehl, welche Versionen von Azure PowerShell derzeit installiert sind:</span><span class="sxs-lookup"><span data-stu-id="f6430-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="f6430-113">Das folgende Skript fragt den PowerShell-Katalog ab, um eine Liste mit den abhängigen Submodulen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6430-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="f6430-114">Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="f6430-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="f6430-115">Sie benötigen Administratorzugriff, um dieses Skript in einem anderen Bereich als `Process` oder `CurrentUser` auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f6430-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="f6430-116">Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="f6430-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="f6430-117">Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version von Azure PowerShell zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f6430-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="f6430-118">Bei der Ausführung des Skripts werden jeweils der Name und die Version des Submoduls angezeigt, das gerade deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="f6430-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="f6430-119">Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, verwenden Sie die Option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="f6430-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="f6430-120">Führen Sie diesen Befehl für jede Azure PowerShell-Version aus, die Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f6430-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="f6430-121">Der Einfachheit halber werden mit dem folgenden Skript alle Versionen von Az deinstalliert, __mit Ausnahme__ der aktuellen Version.</span><span class="sxs-lookup"><span data-stu-id="f6430-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="f6430-122">Deinstallieren des AzureRM-Moduls</span><span class="sxs-lookup"><span data-stu-id="f6430-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="f6430-123">Falls Sie das Az-Modul auf Ihrem System installiert haben und AzureRM deinstallieren möchten, haben Sie zwei Möglichkeiten, bei denen das obige `Uninstall-AllModules`-Skript nicht ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f6430-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two simple options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="f6430-124">Die Wahl der Methode richtet sich danach, wie Sie AzureRM installiert haben.</span><span class="sxs-lookup"><span data-stu-id="f6430-124">Which method you follow depends on how you installed AzureRM.</span></span>
<span data-ttu-id="f6430-125">Wenn Sie nicht sicher sind, sollten Sie zuerst die Schritte zum Deinstallieren einer MSI überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f6430-125">If you're not sure, check the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-msi"></a><span data-ttu-id="f6430-126">Deinstallieren einer MSI</span><span class="sxs-lookup"><span data-stu-id="f6430-126">Uninstall MSI</span></span>

<span data-ttu-id="f6430-127">Falls Sie die AzureRM-Module von Azure PowerShell mit dem MSI-Paket installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System durchführen.</span><span class="sxs-lookup"><span data-stu-id="f6430-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="f6430-128">Plattform</span><span class="sxs-lookup"><span data-stu-id="f6430-128">Platform</span></span> | <span data-ttu-id="f6430-129">Anleitung</span><span class="sxs-lookup"><span data-stu-id="f6430-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="f6430-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f6430-130">Windows 10</span></span> | <span data-ttu-id="f6430-131">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="f6430-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="f6430-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6430-132">Windows 7</span></span> </br><span data-ttu-id="f6430-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f6430-133">Windows 8</span></span> | <span data-ttu-id="f6430-134">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="f6430-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="f6430-135">Auf diesem Bildschirm sollte „Azure PowerShell“ in der Programmliste aufgeführt sein. Sie können die Anwendung dort deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="f6430-135">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="f6430-136">Deinstallieren über PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6430-136">Uninstall from PowerShell</span></span>

<span data-ttu-id="f6430-137">Falls Sie AzureRM über PowerShellGet installiert haben, können Sie die Module mit dem neuen Befehl `Uninstall-AzureRM` entfernen.</span><span class="sxs-lookup"><span data-stu-id="f6430-137">If you installed AzureRM from PowerShellGet, then you can remove the modules with the new `Uninstall-AzureRM` command.</span></span> <span data-ttu-id="f6430-138">Hiermit werden _alle_ AzureRM-Module von Ihrem Computer entfernt, aber für diesen Vorgang werden Administratorrechte benötigt.</span><span class="sxs-lookup"><span data-stu-id="f6430-138">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="f6430-139">Wenn Sie den Befehl `Uninstall-AzureRM` nicht erfolgreich ausführen können, können Sie stattdessen das in diesem Artikel enthaltene `Uninstall-AllModules`-Skript verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6430-139">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>