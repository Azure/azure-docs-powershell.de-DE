---
title: Deinstallieren von Azure PowerShell
description: Anleitung zum vollständigen Deinstallieren von Azure PowerShell
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 17a9b604da84f131c434e3001732a34f7d620fbd
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243581"
---
# <a name="uninstall-the-azure-powershell-module"></a>Deinstallieren des Azure PowerShell-Moduls

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

In diesem Artikel erfahren Sie, wie Sie eine ältere Version von Azure PowerShell deinstallieren bzw. vollständig vom System entfernen. Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um uns Feedback zu senden, falls Sie Azure PowerShell vollständig deinstallieren möchten.
Falls ein Fehler aufgetreten ist, wären wir Ihnen dankbar, wenn Sie ein [GitHub-Problem melden](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi-or-web-platform-installer"></a>Deinstallieren des MSI-Pakets oder des Webplattform-Installers

Falls Sie Azure PowerShell mithilfe des MSI-Pakets oder des Webplattform-Installers installiert haben, müssen Sie die Deinstallation nicht über PowerShell, sondern über das Windows-System durchführen.

| Plattform | Instructions |
|----------|--------------|
| Windows 10 | Start > Einstellungen > Apps |
| Windows 7 </br>Windows 8 | Start > Systemsteuerung > Programme > Programm deinstallieren |

Auf diesem Bildschirm sollte „Azure PowerShell“ in der Programmliste aufgeführt sein. Sie können die Anwendung dort deinstallieren.

## <a name="uninstall-from-powershell"></a>Deinstallieren über PowerShell

Falls Sie Azure PowerShell mithilfe von PowerShellGet installiert haben, können Sie das Cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module) verwenden. Mit `Uninstall-Module` wird jedoch nur ein Modul deinstalliert. Wenn Sie Azure PowerShell vollständig entfernen möchten, müssen Sie die Module einzeln deinstallieren. Die Deinstallation kann kompliziert sein, wenn mehrere Versionen von Azure PowerShell installiert sind.

Sie können das folgende Skript verwenden, um eine einzelne Version von Azure PowerShell vollständig zu entfernen. Das Skript fragt den PowerShell-Katalog ab, um eine Liste der abhängigen Submodule abzurufen. Anschließend wird mit dem Skript die richtige Version der einzelnen Submodule deinstalliert.

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

Kopieren Sie zum Verwenden dieser Funktion den Code, und fügen Sie ihn in Ihre PowerShell-Sitzung ein. Das folgende Beispiel zeigt, wie Sie die Funktion ausführen, um eine ältere Version von Azure PowerShell zu entfernen.

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Bei der Ausführung des Skripts werden jeweils der Name und die Version des Submoduls angezeigt, das gerade deinstalliert wird. Wenn Sie das Skript nur ausführen möchten, um zu ermitteln, welche Elemente gelöscht werden, ohne sie jedoch tatsächlich zu löschen, verwenden Sie die Option `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> Wenn das Skript keine Abhängigkeit mit der genauen Version findet, die deinstalliert werden soll, wird _keine_ Version dieser Abhängigkeit deinstalliert. Dies ist darauf zurückzuführen, dass möglicherweise andere Versionen des Zielmoduls in Ihrem System vorhanden sind, die auf diesen Abhängigkeiten beruhen. In diesem Fall werden die verfügbaren Versionen der Abhängigkeit aufgelistet.
> Sie können dann ältere Versionen manuell mit `Uninstall-Module` entfernen.


Führen Sie diesen Befehl für jede Azure PowerShell-Version aus, die Sie deinstallieren möchten. Der Einfachheit halber deinstalliert das folgende Skript alle AzureRM-Versionen __mit Ausnahme__ der aktuellen Version.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
