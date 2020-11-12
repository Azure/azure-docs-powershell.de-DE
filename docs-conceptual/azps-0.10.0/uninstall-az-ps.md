---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ff9135839b01ad9a1bf10e5969cd3226fe492145
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408852"
---
# <a name="uninstall-the-azure-powershell-module"></a>Deinstallieren des Azure PowerShell-Moduls

In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen. Verwenden Sie das Cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback), um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten. Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues), damit es behoben werden kann.

## <a name="uninstall-the-az-powershell-module-from-msi"></a>Deinstallieren des Azure PowerShell-Moduls über MSI

Falls Sie das Azure PowerShell-Modul mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.

|         Plattform         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start > Einstellungen > Apps                                |
| Windows 7 </br>Windows 8 | Start > Systemsteuerung > Programme > Programm deinstallieren |

Auf diesem Bildschirm sollte **Azure PowerShell** in der Programmliste aufgeführt sein. Dies ist die App, die deinstalliert werden soll. Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a>Deinstallieren des Az PowerShell-Moduls über PowerShellGet

Zum Deinstallieren der Az-Module können Sie das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module) verwenden. Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert. Wenn Sie das Az PowerShell-Modul vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren. Die Deinstallation kann kompliziert sein, wenn Sie mehrere Versionen von Azure PowerShell installiert haben.

Überprüfen Sie mit dem folgenden Befehl, welche Versionen des Az PowerShell-Moduls installiert sind:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

Das folgende Skript fragt den PowerShell-Katalog ab, um eine Liste mit den abhängigen Submodulen abzurufen. Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert. Sie benötigen Administratorzugriff, um dieses Skript in einem anderen Bereich als **Prozess** oder **Aktueller Benutzer** auszuführen.

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

Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein. Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version des Az PowerShell-Moduls und seine Untermodule zu entfernen.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

Bei der Ausführung des Skripts werden jeweils **Name** , **Version** und **Status** des Submoduls angezeigt, das gerade deinstalliert wird. Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, geben Sie den Parameter `-WhatIf` an.

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
> Wenn das Skript keine Abhängigkeit mit der genauen Version findet, die deinstalliert werden soll, wird _keine_ Version dieser Abhängigkeit deinstalliert. Dies ist darauf zurückzuführen, dass möglicherweise andere Versionen des Zielmoduls in Ihrem System vorhanden sind, die auf diesen Abhängigkeiten beruhen.

Führen Sie das folgende Beispiel für jede Version des Az PowerShell-Moduls aus, die Sie deinstallieren möchten.
Der Einfachheit halber werden mit dem folgenden Skript alle Versionen von Az deinstalliert, **mit Ausnahme** der aktuellen Version.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>Deinstallieren des AzureRM-Moduls

Falls Sie das Az-Modul auf Ihrem System installiert haben und AzureRM deinstallieren möchten, haben Sie zwei Möglichkeiten. Die Wahl der Methode richtet sich danach, wie Sie das AzureRM-Modul installiert haben. Wenn Sie sich bezüglich Ihrer ursprünglichen Installationsmethode nicht sicher sind, befolgen Sie zuerst die Schritte zur Deinstallation einer MSI.

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a>Deinstallieren des AzureRM PowerShell-Moduls über MSI

Falls Sie das AzureRM PowerShell-Modul mithilfe des MSI-Pakets installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System ausführen.

|         Plattform         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start > Einstellungen > Apps                                |
| Windows 7 </br>Windows 8 | Start > Systemsteuerung > Programme > Programm deinstallieren |

Auf dem angezeigten Bildschirm sollte in der Programmliste **Azure PowerShell** oder **Microsoft Azure PowerShell – Monat/Jahr** aufgeführt sein. Dies ist die App, die deinstalliert werden soll. Ist dieses Programm nicht aufgeführt, haben Sie für die Installation PowerShellGet verwendet und müssen die folgenden Anweisungen befolgen.

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a>Deinstallieren des AzureRM PowerShell-Moduls über PowerShellGet

Wenn Sie AzureRM mit PowerShellGet installiert haben, können Sie die Module mit dem Cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) (als Teil des `Az.Accounts`-Moduls verfügbar) entfernen. Mit dem folgenden Beispiel werden _alle_ AzureRM-Module von Ihrem Computer entfernt. Für diesen Vorgang sind Administratorrechte erforderlich.

```powershell-interactive
Uninstall-AzureRm
```
