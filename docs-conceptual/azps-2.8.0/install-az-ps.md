---
title: Installieren von Azure PowerShell mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2019
ms.locfileid: "72814227"
---
# <a name="install-the-azure-powershell-module"></a>Installieren des Azure PowerShell-Moduls

In diesem Artikel erfahren Sie, wie Sie mithilfe von „PowerShellGet“ die Azure PowerShell-Module installieren. Diese Anweisungen können für Windows-, macOS- und Linux-Plattformen verwendet werden. Für das Az-Modul werden derzeit keine anderen Installationsmethoden unterstützt.

## <a name="requirements"></a>Requirements (Anforderungen)

Azure PowerShell kann mit PowerShell 5.1 oder höher unter Windows oder mit PowerShell Core 6.x und höher auf allen Plattformen verwendet werden. Wenn Sie sich nicht sicher sind, ob Sie über PowerShell verfügen oder unter MacOS oder Linux arbeiten, [installieren Sie die neueste Version von PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:

```powershell-interactive
$PSVersionTable.PSVersion
```

So führen Sie Azure PowerShell in PowerShell 5.1 unter Windows aus

1. Führen Sie bei Bedarf ein Update auf [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus. Unter Windows 10 ist PowerShell 5.1 bereits installiert.
2. Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).

Bei Verwendung von PowerShell Core gibt es keine zusätzlichen Anforderungen an Azure PowerShell.

## <a name="install-the-azure-powershell-module"></a>Installieren des Azure PowerShell-Moduls

> [!WARNING]
> Die Module AzureRM und Az können für PowerShell 5.1 für Windows __nicht__ gleichzeitig installiert sein. Wenn AzureRM weiterhin auf Ihrem System verfügbar sein soll, installieren Sie das Az-Modul für PowerShell Core 6.x oder höher. Installieren Sie dazu [PowerShell Core 6.x oder höher](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows), und befolgen Sie dann diese Anweisungen in einem PowerShell Core-Terminal.

Es wird empfohlen, die Installation nur für den aktiven Benutzer auszuführen:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Für die Installation für alle Benutzer in einem System sind Administratorberechtigungen erforderlich. Führen Sie unter macOS oder Linux Folgendes in einer PowerShell-Sitzung mit erhöhten Rechten aus (entweder als Administrator oder mithilfe des Befehls `sudo`):

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert. Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.

Das Az-Modul ist ein Rollupmodul für die Azure PowerShell-Cmdlets. Wenn Sie es installieren, werden alle verfügbaren Azure Resource Manager-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.

## <a name="install-offline"></a>Offlineinstallation

In einigen Umgebungen ist es nicht möglich, eine Verbindung mit dem PowerShell-Katalog herzustellen. In diesen Fällen können Sie die Installation mithilfe einer der folgenden Methoden weiterhin offline durchführen:

* Laden Sie die Module an einen anderen Speicherort herunter, und verwenden Sie diesen als Installationsquelle in Ihrem Netzwerk. Dieser Prozess kann zwar etwas kompliziert sein, ermöglicht aber die Zwischenspeicherung von PowerShell-Modulen, die mithilfe von PowerShellGet auf Systemen ohne Verbindung bereitgestellt werden sollen, auf einem einzelnen Server oder in einer einzelnen Dateifreigabe. Unter [Arbeiten mit lokalen PowerShellGet-Repositorys](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) erfahren Sie, wie Sie ein lokales Repository einrichten und die Installation auf getrennten Systemen ausführen.
* [Laden Sie die Azure PowerShell MSI](install-az-ps-msi.md) auf einen mit dem Netzwerk verbundenen Computer herunter, und kopieren Sie anschließend das Installationsprogramm auf Systeme ohne Zugriff auf den PowerShell-Katalog. Beachten Sie, dass das MSI-Installationsprogramm nur für PowerShell 5.1 unter Windows verwendet werden kann.
* Speichern Sie das Modul mit [Save-Module](/powershell/module/PowershellGet/Save-Module) auf einer Dateifreigabe oder einer anderen Quelle, und kopieren Sie es manuell auf andere Computer:
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Problembehandlung

In diesem Abschnitt finden Sie einige allgemeine Probleme, die bei der Installation des Azure PowerShell-Moduls auftreten können. Falls ein Problem auftritt, das hier nicht aufgeführt ist, [melden Sie es auf GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Der Proxy blockiert die Verbindung.

Wenn Sie von `Install-Module` Fehler erhalten, die anzeigen, dass der PowerShell-Katalog nicht erreichbar ist, befinden Sie sich möglicherweise hinter einem Proxy. Verschiedene Betriebssysteme haben unterschiedliche Anforderungen an die Konfiguration eines systemweiten Proxys, die hier nicht ausführlich behandelt werden. Wenden Sie sich an Ihren Systemadministrator, um Ihre Proxyeinstellungen zu erhalten und zu erfahren, wie Sie sie für Ihr Betriebssystem konfigurieren können.

PowerShell selbst ist möglicherweise nicht so konfiguriert, dass es diesen Proxy automatisch verwendet. Konfigurieren Sie den Proxy für PowerShell 5.1 und höher mit dem folgenden Befehl so, dass er eine PowerShell-Sitzung verwendet:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Wenn die Anmeldeinformationen Ihres Betriebssystems ordnungsgemäß konfiguriert sind, werden PowerShell-Anforderungen über den Proxy weitergeleitet.
Damit diese Einstellung auch zwischen den Sitzungen erhalten bleibt, fügen Sie den Befehl zu einem [PowerShell-Profil](/powershell/module/microsoft.powershell.core/about/about_profiles) hinzu.

Ihr Proxy muss HTTPS-Verbindungen zu der folgenden Adresse zulassen, damit das Paket installiert werden kann:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Anmelden

Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Wenn Sie das automatische Laden von Modulen deaktiviert haben, importieren Sie das Modul manuell mit `Import-Module Az`. Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.

Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualisieren des Azure PowerShell-Moduls

Aufgrund der Art und Weise, wie das Az-Modul gepackt ist, aktualisiert der Befehl [Update-Module](/powershell/module/powershellget/update-module) Ihre Installation nicht ordnungsgemäß. Bei der Installation des Az-Moduls werden alle abhängigen Submodule gesammelt und installiert und dadurch die Cmdlets für jeden Dienst bereitgestellt.
Das bedeutet, dass zum Aktualisieren des Azure PowerShell-Moduls eine __Neuinstallation__ und keine __Aktualisierung__ erforderlich ist. Dies erfolgt auf dieselbe Weise wie bei der Installation, aber Sie müssen möglicherweise das Argument `-Force` hinzufügen:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Obwohl dadurch installierte Module überschrieben werden können, verbleiben möglicherweise noch ältere Versionen auf Ihrem System.
Wenn Sie frühere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md) weiter.

## <a name="use-multiple-versions-of-azure-powershell"></a>Verwenden von mehreren Versionen von Azure PowerShell

Es ist möglich, mehr als eine Version von Azure PowerShell zu installieren. Verwenden Sie den folgenden Befehl zum Überprüfen, ob Sie mehrere Versionen von Azure PowerShell installiert haben:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Anweisungen zum Entfernen einer Version von Azure PowerShell finden Sie unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md).

Wenn Sie eine bestimmte Version des `Az`-Moduls installieren oder laden möchten, können Sie das Argument `-RequiredVersion` verwenden:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Sind mehrere Versionen des Moduls installiert, wird mit der Funktion zum automatischen Laden von Modulen und mit `Import-Module` standardmäßig die neueste Version geladen.

## <a name="provide-feedback"></a>Feedback geben

[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden.
Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).
Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.
