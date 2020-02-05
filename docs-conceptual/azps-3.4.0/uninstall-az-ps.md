---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 10/22/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 37f152fb43e23c361544db4a738d58911099da1f
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002723"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="90bbb-103">Deinstallieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="90bbb-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="90bbb-104">In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="90bbb-105">Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="90bbb-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="90bbb-106">Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues), damit es behoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="90bbb-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="90bbb-107">Deinstallieren von Azure PowerShell über die MSI</span><span class="sxs-lookup"><span data-stu-id="90bbb-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="90bbb-108">Falls Sie Azure PowerShell mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="90bbb-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="90bbb-109">Platform</span></span> | <span data-ttu-id="90bbb-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="90bbb-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="90bbb-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="90bbb-111">Windows 10</span></span> | <span data-ttu-id="90bbb-112">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="90bbb-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="90bbb-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90bbb-113">Windows 7</span></span> </br><span data-ttu-id="90bbb-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="90bbb-114">Windows 8</span></span> | <span data-ttu-id="90bbb-115">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="90bbb-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="90bbb-116">Auf diesem Bildschirm sollte __Azure PowerShell__ in der Programmliste aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="90bbb-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="90bbb-117">Dies ist die App, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90bbb-117">This is the app to uninstall.</span></span> <span data-ttu-id="90bbb-118">Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="90bbb-119">Deinstallieren von Azure PowerShell über PowerShell Get</span><span class="sxs-lookup"><span data-stu-id="90bbb-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="90bbb-120">Verwenden Sie zum Deinstallieren der Az-Module das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="90bbb-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="90bbb-121">Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="90bbb-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="90bbb-122">Wenn Sie Azure PowerShell vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="90bbb-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="90bbb-123">Die Deinstallation kann kompliziert sein, wenn Sie mehrere Versionen von Azure PowerShell installiert haben.</span><span class="sxs-lookup"><span data-stu-id="90bbb-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="90bbb-124">Überprüfen Sie mit dem folgenden Befehl, welche Versionen von Azure PowerShell derzeit installiert sind:</span><span class="sxs-lookup"><span data-stu-id="90bbb-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="90bbb-125">Das folgende Skript fragt den PowerShell-Katalog ab, um eine Liste mit den abhängigen Submodulen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="90bbb-126">Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="90bbb-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="90bbb-127">Sie benötigen Administratorzugriff, um dieses Skript in einem anderen Bereich als `Process` oder `CurrentUser` auszuführen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="90bbb-128">Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="90bbb-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="90bbb-129">Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version von Azure PowerShell zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="90bbb-130">Bei der Ausführung des Skripts werden jeweils der Name und die Version des Submoduls angezeigt, das gerade deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="90bbb-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="90bbb-131">Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, verwenden Sie die Option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="90bbb-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="90bbb-132">Wenn das Skript keine Abhängigkeit mit der genauen Version findet, die deinstalliert werden soll, wird _keine_ Version dieser Abhängigkeit deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="90bbb-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="90bbb-133">Dies ist darauf zurückzuführen, dass möglicherweise andere Versionen des Zielmoduls in Ihrem System vorhanden sind, die auf diesen Abhängigkeiten beruhen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="90bbb-134">In diesem Fall werden die verfügbaren Versionen der Abhängigkeit aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="90bbb-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="90bbb-135">Sie können dann ältere Versionen manuell mit `Uninstall-Module` entfernen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="90bbb-136">Führen Sie diesen Befehl für jede Azure PowerShell-Version aus, die Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="90bbb-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="90bbb-137">Der Einfachheit halber werden mit dem folgenden Skript alle Versionen von Az deinstalliert, __mit Ausnahme__ der aktuellen Version.</span><span class="sxs-lookup"><span data-stu-id="90bbb-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="90bbb-138">Deinstallieren des AzureRM-Moduls</span><span class="sxs-lookup"><span data-stu-id="90bbb-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="90bbb-139">Falls Sie das Az-Modul auf Ihrem System installiert haben und AzureRM deinstallieren möchten, haben Sie zwei Möglichkeiten, bei denen das obige `Uninstall-AllModules`-Skript nicht ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="90bbb-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="90bbb-140">Die Wahl der Methode richtet sich danach, wie Sie das AzureRM-Modul installiert haben.</span><span class="sxs-lookup"><span data-stu-id="90bbb-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="90bbb-141">Wenn Sie sich bezüglich Ihrer ursprünglichen Installationsmethode nicht sicher sind, befolgen Sie zuerst die Schritte zur Deinstallation einer MSI.</span><span class="sxs-lookup"><span data-stu-id="90bbb-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="90bbb-142">Deinstallieren von Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="90bbb-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="90bbb-143">Falls Sie die AzureRM-Module von Azure PowerShell mit dem MSI-Paket installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System durchführen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="90bbb-144">Plattform</span><span class="sxs-lookup"><span data-stu-id="90bbb-144">Platform</span></span> | <span data-ttu-id="90bbb-145">Instructions</span><span class="sxs-lookup"><span data-stu-id="90bbb-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="90bbb-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="90bbb-146">Windows 10</span></span> | <span data-ttu-id="90bbb-147">Start > Einstellungen > Apps</span><span class="sxs-lookup"><span data-stu-id="90bbb-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="90bbb-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90bbb-148">Windows 7</span></span> </br><span data-ttu-id="90bbb-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="90bbb-149">Windows 8</span></span> | <span data-ttu-id="90bbb-150">Start > Systemsteuerung > Programme > Programm deinstallieren</span><span class="sxs-lookup"><span data-stu-id="90bbb-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="90bbb-151">Auf dem angezeigten Bildschirm sollte in der Programmliste __Azure PowerShell__ oder __Microsoft Azure PowerShell – Monat/Jahr__ aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="90bbb-151">Once on this screen you should see __Azure PowerShell__ or __Microsoft Azure PowerShell - Month Year__ in the program listing.</span></span> <span data-ttu-id="90bbb-152">Dies ist die App, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90bbb-152">This is the app to uninstall.</span></span> <span data-ttu-id="90bbb-153">Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="90bbb-154">Deinstallieren über PowerShell</span><span class="sxs-lookup"><span data-stu-id="90bbb-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="90bbb-155">Wenn Sie AzureRM mit PowerShellGet installiert haben, können Sie die Module mit dem Befehl [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) (als Teil des `Az.Accounts`-Moduls verfügbar) entfernen.</span><span class="sxs-lookup"><span data-stu-id="90bbb-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="90bbb-156">Hiermit werden _alle_ AzureRM-Module von Ihrem Computer entfernt, aber für diesen Vorgang werden Administratorrechte benötigt.</span><span class="sxs-lookup"><span data-stu-id="90bbb-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
<span data-ttu-id="90bbb-157">oder</span><span class="sxs-lookup"><span data-stu-id="90bbb-157">or</span></span>
```powershell-interactive
Uninstall-Module AzureRm
```

<span data-ttu-id="90bbb-158">Wenn Sie den Befehl `Uninstall-AzureRM` nicht erfolgreich ausführen können, können Sie stattdessen das in diesem Artikel enthaltene [`Uninstall-AllModules`-Skript](#uninstall-script) mit folgendem Aufruf verwenden:</span><span class="sxs-lookup"><span data-stu-id="90bbb-158">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
<span data-ttu-id="90bbb-159">oder</span><span class="sxs-lookup"><span data-stu-id="90bbb-159">or</span></span>
```powershell-interactive
foreach ($module in (Get-Module -ListAvailable AzureRM*).Name |Get-Unique) {
   write-host "Removing Module $module"
   Uninstall-module $module
}
```
