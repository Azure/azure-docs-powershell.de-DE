---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8b6a96c89b37708646b24f2f2f82a10537dd0ee5
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241813"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="c3756-103">Deinstallieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="c3756-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="c3756-104">In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3756-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="c3756-105">Verwenden Sie das Cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback), um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c3756-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="c3756-106">Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues), damit es behoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3756-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="c3756-107">Deinstallieren des Azure PowerShell-Moduls über MSI</span><span class="sxs-lookup"><span data-stu-id="c3756-107">Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="c3756-108">Falls Sie das Azure PowerShell-Modul mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3756-108">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="c3756-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="c3756-109">Platform</span></span>         |                      <span data-ttu-id="c3756-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="c3756-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="c3756-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3756-111">Windows 10</span></span>               | <span data-ttu-id="c3756-112">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="c3756-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="c3756-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3756-113">Windows 7</span></span> </br><span data-ttu-id="c3756-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3756-114">Windows 8</span></span> | <span data-ttu-id="c3756-115">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="c3756-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="c3756-116">Auf diesem Bildschirm sollte **Azure PowerShell** in der Programmliste aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="c3756-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="c3756-117">Dies ist die App, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3756-117">This is the app to uninstall.</span></span> <span data-ttu-id="c3756-118">Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="c3756-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="c3756-119">Deinstallieren des Az PowerShell-Moduls über PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="c3756-119">Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="c3756-120">Zum Deinstallieren der Az-Module können Sie das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3756-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="c3756-121">Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="c3756-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="c3756-122">Wenn Sie das Az PowerShell-Modul vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="c3756-122">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="c3756-123">Die Deinstallation kann kompliziert sein, wenn Sie mehrere Versionen von Azure PowerShell installiert haben.</span><span class="sxs-lookup"><span data-stu-id="c3756-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="c3756-124">Überprüfen Sie mit dem folgenden Befehl, welche Versionen des Az PowerShell-Moduls installiert sind:</span><span class="sxs-lookup"><span data-stu-id="c3756-124">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

<span data-ttu-id="c3756-125">Das folgende Skript fragt den PowerShell-Katalog ab, um eine Liste mit den abhängigen Submodulen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3756-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="c3756-126">Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="c3756-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="c3756-127">Sie benötigen Administratorzugriff, um dieses Skript in einem anderen Bereich als **Prozess** oder **Aktueller Benutzer** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c3756-127">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="c3756-128">Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="c3756-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="c3756-129">Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version des Az PowerShell-Moduls und seine Untermodule zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3756-129">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="c3756-130">Bei der Ausführung des Skripts werden jeweils **Name**, **Version** und **Status** des Submoduls angezeigt, das gerade deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="c3756-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="c3756-131">Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, geben Sie den Parameter `-WhatIf` an.</span><span class="sxs-lookup"><span data-stu-id="c3756-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="c3756-132">Wenn das Skript keine Abhängigkeit mit der genauen Version findet, die deinstalliert werden soll, wird _keine_ Version dieser Abhängigkeit deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="c3756-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="c3756-133">Dies ist darauf zurückzuführen, dass möglicherweise andere Versionen des Zielmoduls in Ihrem System vorhanden sind, die auf diesen Abhängigkeiten beruhen.</span><span class="sxs-lookup"><span data-stu-id="c3756-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="c3756-134">Führen Sie das folgende Beispiel für jede Version des Az PowerShell-Moduls aus, die Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c3756-134">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="c3756-135">Der Einfachheit halber werden mit dem folgenden Skript alle Versionen von Az deinstalliert, **mit Ausnahme** der aktuellen Version.</span><span class="sxs-lookup"><span data-stu-id="c3756-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="c3756-136">Deinstallieren des AzureRM-Moduls</span><span class="sxs-lookup"><span data-stu-id="c3756-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="c3756-137">Falls Sie das Az-Modul auf Ihrem System installiert haben und AzureRM deinstallieren möchten, haben Sie zwei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="c3756-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="c3756-138">Die Wahl der Methode richtet sich danach, wie Sie das AzureRM-Modul installiert haben.</span><span class="sxs-lookup"><span data-stu-id="c3756-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="c3756-139">Wenn Sie sich bezüglich Ihrer ursprünglichen Installationsmethode nicht sicher sind, befolgen Sie zuerst die Schritte zur Deinstallation einer MSI.</span><span class="sxs-lookup"><span data-stu-id="c3756-139">If you're not sure of your original installation method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="c3756-140">Deinstallieren des AzureRM PowerShell-Moduls über MSI</span><span class="sxs-lookup"><span data-stu-id="c3756-140">Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="c3756-141">Falls Sie das AzureRM PowerShell-Modul mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3756-141">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="c3756-142">Plattform</span><span class="sxs-lookup"><span data-stu-id="c3756-142">Platform</span></span>         |                      <span data-ttu-id="c3756-143">Instructions</span><span class="sxs-lookup"><span data-stu-id="c3756-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="c3756-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3756-144">Windows 10</span></span>               | <span data-ttu-id="c3756-145">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="c3756-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="c3756-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3756-146">Windows 7</span></span> </br><span data-ttu-id="c3756-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3756-147">Windows 8</span></span> | <span data-ttu-id="c3756-148">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="c3756-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="c3756-149">Auf dem angezeigten Bildschirm sollte in der Programmliste **Azure PowerShell** oder **Microsoft Azure PowerShell – Monat/Jahr** aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="c3756-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="c3756-150">Dies ist die App, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3756-150">This is the app to uninstall.</span></span> <span data-ttu-id="c3756-151">Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="c3756-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="c3756-152">Deinstallieren des AzureRM PowerShell-Moduls über PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="c3756-152">Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="c3756-153">Wenn Sie AzureRM mit PowerShellGet installiert haben, können Sie die Module mit dem Cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) (als Teil des `Az.Accounts`-Moduls verfügbar) entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3756-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="c3756-154">Mit dem folgenden Beispiel werden _alle_ AzureRM-Module von Ihrem Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="c3756-154">The following example removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="c3756-155">Für diesen Vorgang sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3756-155">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
