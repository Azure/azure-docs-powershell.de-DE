---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7f831bdf6d6144640e036d72900958847283acf1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002125"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="6e448-103">Anleitung zum Deinstallieren von Azure PowerShell-Modulen</span><span class="sxs-lookup"><span data-stu-id="6e448-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="6e448-104">In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen.</span><span class="sxs-lookup"><span data-stu-id="6e448-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="6e448-105">Verwenden Sie das Cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback), um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6e448-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="6e448-106">Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues), damit es behoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e448-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="6e448-107">Deinstallieren des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="6e448-107">Uninstall the Az module</span></span>

<span data-ttu-id="6e448-108">Falls Sie das Az-Modul auf Ihrem System installiert haben und es deinstallieren möchten, haben Sie zwei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="6e448-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="6e448-109">Die Wahl der Methode richtet sich danach, wie Sie das Az-Modul installiert haben.</span><span class="sxs-lookup"><span data-stu-id="6e448-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="6e448-110">Wenn Sie sich bezüglich Ihrer ursprünglichen Installationsmethode nicht sicher sind, befolgen Sie zuerst die MSI-Schritte zur Deinstallation.</span><span class="sxs-lookup"><span data-stu-id="6e448-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="6e448-111">Option 1: Deinstallieren des Azure PowerShell-Moduls über MSI</span><span class="sxs-lookup"><span data-stu-id="6e448-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="6e448-112">Falls Sie das Azure PowerShell-Modul mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e448-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="6e448-113">Plattform</span><span class="sxs-lookup"><span data-stu-id="6e448-113">Platform</span></span>         |                      <span data-ttu-id="6e448-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="6e448-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="6e448-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6e448-115">Windows 10</span></span>               | <span data-ttu-id="6e448-116">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="6e448-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="6e448-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e448-117">Windows 7</span></span> </br><span data-ttu-id="6e448-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e448-118">Windows 8</span></span> | <span data-ttu-id="6e448-119">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="6e448-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="6e448-120">Auf diesem Bildschirm sollte **Azure PowerShell** in der Programmliste aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="6e448-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="6e448-121">Dies ist die App, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e448-121">This is the app to uninstall.</span></span> <span data-ttu-id="6e448-122">Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="6e448-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="6e448-123">Option 2: Deinstallieren des Az PowerShell-Moduls über PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="6e448-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="6e448-124">Zum Deinstallieren der Az-Module können Sie das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module) verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e448-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="6e448-125">Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="6e448-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="6e448-126">Wenn Sie das Az PowerShell-Modul vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="6e448-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="6e448-127">Die Deinstallation kann kompliziert sein, wenn Sie mehrere Versionen von Azure PowerShell installiert haben.</span><span class="sxs-lookup"><span data-stu-id="6e448-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="6e448-128">Überprüfen Sie mit dem folgenden Befehl, welche Versionen des Az PowerShell-Moduls installiert sind:</span><span class="sxs-lookup"><span data-stu-id="6e448-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="6e448-129">Das folgende Skript fragt den PowerShell-Katalog ab, um eine Liste mit den abhängigen Submodulen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e448-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="6e448-130">Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="6e448-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="6e448-131">Sie benötigen Administratorzugriff, um dieses Skript in einem anderen Bereich als **Prozess** oder **Aktueller Benutzer** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6e448-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

<span data-ttu-id="6e448-132">Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="6e448-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="6e448-133">Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version des Az PowerShell-Moduls und seine Untermodule zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6e448-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="6e448-134">Bei der Ausführung des Skripts werden jeweils **Name**, **Version** und **Status** des Submoduls angezeigt, das gerade deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="6e448-134">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="6e448-135">Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, geben Sie den Parameter `-WhatIf` an.</span><span class="sxs-lookup"><span data-stu-id="6e448-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> <span data-ttu-id="6e448-136">Wenn das Skript keine Abhängigkeit mit der genauen Version findet, die deinstalliert werden soll, wird _keine_ Version dieser Abhängigkeit deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="6e448-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="6e448-137">Dies ist darauf zurückzuführen, dass möglicherweise andere Versionen des Zielmoduls in Ihrem System vorhanden sind, die auf diesen Abhängigkeiten beruhen.</span><span class="sxs-lookup"><span data-stu-id="6e448-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="6e448-138">Führen Sie das folgende Beispiel für jede Version des Az PowerShell-Moduls aus, die Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6e448-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="6e448-139">Der Einfachheit halber werden mit dem folgenden Skript alle Versionen von Az deinstalliert, **mit Ausnahme** der aktuellen Version.</span><span class="sxs-lookup"><span data-stu-id="6e448-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="6e448-140">Deinstallieren des AzureRM-Moduls</span><span class="sxs-lookup"><span data-stu-id="6e448-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="6e448-141">Falls Sie das Az-Modul auf Ihrem System installiert haben und AzureRM deinstallieren möchten, haben Sie zwei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="6e448-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="6e448-142">Die Wahl der Methode richtet sich danach, wie Sie das AzureRM-Modul installiert haben.</span><span class="sxs-lookup"><span data-stu-id="6e448-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="6e448-143">Wenn Sie sich bezüglich Ihrer ursprünglichen Installationsmethode nicht sicher sind, befolgen Sie zuerst die MSI-Schritte zur Deinstallation.</span><span class="sxs-lookup"><span data-stu-id="6e448-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="6e448-144">Option 1: Deinstallieren des AzureRM PowerShell-Moduls über MSI</span><span class="sxs-lookup"><span data-stu-id="6e448-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="6e448-145">Falls Sie das AzureRM PowerShell-Modul mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e448-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="6e448-146">Plattform</span><span class="sxs-lookup"><span data-stu-id="6e448-146">Platform</span></span>         |                      <span data-ttu-id="6e448-147">Instructions</span><span class="sxs-lookup"><span data-stu-id="6e448-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="6e448-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6e448-148">Windows 10</span></span>               | <span data-ttu-id="6e448-149">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="6e448-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="6e448-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e448-150">Windows 7</span></span> </br><span data-ttu-id="6e448-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e448-151">Windows 8</span></span> | <span data-ttu-id="6e448-152">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="6e448-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="6e448-153">Auf dem angezeigten Bildschirm sollte in der Programmliste **Azure PowerShell** oder **Microsoft Azure PowerShell – Monat/Jahr** aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="6e448-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="6e448-154">Dies ist die App, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e448-154">This is the app to uninstall.</span></span> <span data-ttu-id="6e448-155">Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="6e448-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="6e448-156">Option 2: Deinstallieren des AzureRM PowerShell-Moduls über PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="6e448-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="6e448-157">Wenn Sie AzureRM mit PowerShellGet installiert haben, können Sie die Module mit dem Cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) (als Teil des `Az.Accounts`-Moduls verfügbar) entfernen.</span><span class="sxs-lookup"><span data-stu-id="6e448-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="6e448-158">Damit Sie das Modul `Az.Accounts` verwenden können, muss das Az-Modul installiert sein.</span><span class="sxs-lookup"><span data-stu-id="6e448-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="6e448-159">Das AzureRM- und das Az-Modul können nicht gleichzeitig installiert sein. Das Az-Modul kann jedoch zur sofortigen Deinstallation des AzureRM-Moduls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e448-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="6e448-160">Sie können das Az-Modul installieren und die Warnung des AzureRM-Moduls mit dem folgenden Befehl umgehen, falls das Az-Modul nicht bereits installiert ist:</span><span class="sxs-lookup"><span data-stu-id="6e448-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="6e448-161">Nach der Installation des Az-Moduls werden mit dem folgenden Befehl _alle_ AzureRM-Module vom Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="6e448-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="6e448-162">Für diesen Vorgang sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e448-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
