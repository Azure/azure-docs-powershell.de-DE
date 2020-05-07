---
title: Installieren von Azure PowerShell unter Windows mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 5de386bde1b8be5a4455b85d4f5fcdf38e4fcea2
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65535012"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installieren von Azure PowerShell unter Windows mit PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

In diesem Artikel erfahren Sie, wie Sie die Azure PowerShell-Module für PowerShell 5.x für Windows mit PowerShellGet installieren. PowerShellGet und die Modulverwaltung stellen die bevorzugte Installationsmethode für Azure PowerShell dar. Sie können aber auch den Webplattform-Installer oder das MSI-Paket verwenden. Entsprechende Informationen finden Sie unter [Andere Installationsmethoden](other-install.md).

Das klassische Azure-Bereitstellungsmodell wird von dieser Version von Azure PowerShell nicht unterstützt. Befolgen Sie die Anleitung unter [Installieren des Azure PowerShell-Dienstverwaltungsmoduls](/powershell/azure/servicemanagement/install-azure-ps), um Unterstützung zu klassischen Bereitstellungen zu erhalten.

> [!IMPORTANT]
> Das AzureRM-Modul wird für macOS oder Linux nicht unterstützt. Wenn Sie Azure PowerShell-Cmdlets auf diesen Plattformen verwenden möchten, [installieren Sie das Az-Modul](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Requirements (Anforderungen)

Ab Version 6.0 erfordert Azure PowerShell die PowerShell-Version 5.0. Führen Sie den folgenden Befehl aus, um die Version von PowerShell zu prüfen, die auf Ihrem Computer ausgeführt wird:

```powershell-interactive
$PSVersionTable.PSVersion
```

Falls Sie über eine veraltete Version verfügen, helfen Ihnen die Informationen unter [Aktualisieren einer vorhandenen Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) weiter.

> [!IMPORTANT]
> Das in diesem Dokument beschriebene Modul „AzureRM“ verwendet .NET Framework. Dadurch ist es nicht mit PowerShell 6.0 kompatibel, das .NET Core verwendet. Wenn Sie PowerShell 6.0 verwenden, befolgen Sie die [Installationsanweisungen für macOS und Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Installieren des Azure PowerShell-Moduls

Sie benötigen erhöhte Rechte, um Module aus dem PowerShell-Katalog installieren zu können. Führen Sie den folgenden Befehl in einer Sitzung mit erhöhten Rechten aus, um Azure PowerShell zu installieren:

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> Wenn Sie eine ältere NuGet-Version als 2.8.5.201 haben, werden Sie aufgefordert, die aktuelle NuGet-Version herunterzuladen und zu installieren.

Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert. Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.

Das Modul `AzureRM` ist ein Rollupmodul für die Azure PowerShell-Cmdlets. Wenn Sie es installieren, werden alle verfügbaren Azure Resource Manager-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.

## <a name="sign-in"></a>Anmelden

Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module AzureRM` importieren. Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.


Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualisieren des Azure PowerShell-Moduls

Sie können Ihre Azure PowerShell-Installation aktualisieren, indem Sie [Update-Module](/powershell/module/powershellget/update-module) ausführen. Mit diesem Befehl werden __keine__ früheren Versionen deinstalliert.

```powershell-interactive
Update-Module -Name AzureRM
```

Wenn Sie ältere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md) (Deinstallieren des Azure PowerShell-Moduls) weiter.

## <a name="use-multiple-versions-of-azure-powershell"></a>Verwenden von mehreren Versionen von Azure PowerShell

Es ist möglich, mehr als eine Version von Azure PowerShell zu installieren. Verwenden Sie den folgenden Befehl zum Überprüfen, ob Sie mehrere Versionen von Azure PowerShell installiert haben:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

Anweisungen zum Entfernen einer Version von Azure PowerShell finden Sie unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-azurerm-ps.md).

Unter Umständen benötigen Sie mehr als eine Version, wenn Sie mit lokalen Azure Stack-Ressourcen arbeiten, eine ältere Version von Windows ausführen oder das klassische Azure-Bereitstellungsmodell nutzen. Geben Sie beim Installieren das Argument `-RequiredVersion` an, um eine ältere Version zu installieren.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Beim Laden des Azure PowerShell-Moduls wird standardmäßig die aktuelle Version geladen. Geben Sie das Argument `-RequiredVersion` an, um eine andere Version zu laden.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Feedback geben

[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie bei der Nutzung von Azure PowerShell einen Fehler finden.
Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zum Modul und zu den zugehörigen Features als Einstieg in die Nutzung von Azure PowerShell finden Sie unter [Get started with Azure PowerShell](get-started-azureps.md) (Erste Schritte mit Azure PowerShell).
