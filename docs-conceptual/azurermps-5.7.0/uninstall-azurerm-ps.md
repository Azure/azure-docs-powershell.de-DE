---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037693"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="ac9fd-103">Deinstallieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="ac9fd-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="ac9fd-104">In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="ac9fd-105">Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="ac9fd-106">Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="ac9fd-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="ac9fd-107">Deinstallieren des MSI-Pakets oder des Webplattform-Installers</span><span class="sxs-lookup"><span data-stu-id="ac9fd-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="ac9fd-108">Falls Sie Azure PowerShell mithilfe des MSI-Pakets oder des Webplattform-Installers installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System durchführen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="ac9fd-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="ac9fd-109">Platform</span></span> | <span data-ttu-id="ac9fd-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="ac9fd-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="ac9fd-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ac9fd-111">Windows 10</span></span> | <span data-ttu-id="ac9fd-112">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="ac9fd-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="ac9fd-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac9fd-113">Windows 7</span></span> </br><span data-ttu-id="ac9fd-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac9fd-114">Windows 8</span></span> | <span data-ttu-id="ac9fd-115">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="ac9fd-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="ac9fd-116">Auf diesem Bildschirm sollte „Azure PowerShell“ in der Programmliste aufgeführt sein. Sie können die Anwendung dort deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="ac9fd-117">Deinstallieren über PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac9fd-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="ac9fd-118">Falls Sie Azure PowerShell mithilfe von PowerShellGet installiert haben, können Sie das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="ac9fd-119">Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="ac9fd-120">Wenn Sie Azure PowerShell vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="ac9fd-121">Die Deinstallation kann kompliziert sein, wenn mehrere Versionen von Azure PowerShell installiert sind.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="ac9fd-122">Sie können das folgende Skript verwenden, um eine einzelne Version von Azure PowerShell vollständig zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="ac9fd-123">Das Skript fragt den PowerShell-Katalog ab, um eine Liste der abhängigen Submodule abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="ac9fd-124">Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

<span data-ttu-id="ac9fd-125">Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="ac9fd-126">Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version von Azure PowerShell zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="ac9fd-127">Bei der Ausführung des Skripts werden jeweils der Name und die Version des Submoduls angezeigt, das gerade deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="ac9fd-128">Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, verwenden Sie die Option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="ac9fd-129">Wenn das Skript keine Abhängigkeit mit der genauen Version findet, die deinstalliert werden soll, wird _keine_ Version dieser Abhängigkeit deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="ac9fd-130">Dies ist darauf zurückzuführen, dass möglicherweise andere Versionen des Zielmoduls in Ihrem System vorhanden sind, die auf diesen Abhängigkeiten beruhen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="ac9fd-131">In diesem Fall werden die verfügbaren Versionen der Abhängigkeit aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="ac9fd-132">Sie können dann ältere Versionen manuell mit `Uninstall-Module` entfernen.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="ac9fd-133">Führen Sie diesen Befehl für jede Azure PowerShell-Version aus, die Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="ac9fd-134">Der Einfachheit halber deinstalliert das folgende Skript alle AzureRM-Versionen __mit Ausnahme__ der aktuellen Version.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
