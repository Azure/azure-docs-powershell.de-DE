---
title: Installieren von Azure PowerShell mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: a263f1d363b3d1a1cce433a6112c55afe65262a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001937"
---
# <a name="install-azure-powershell"></a>Installieren von Azure Powershell

In diesem Artikel wird erläutert, wie Sie mithilfe von [PowerShellGet](/powershell/scripting/gallery/installing-psget) die Azure PowerShell-Module installieren. Diese Anweisungen können für Windows-, macOS- und Linux-Plattformen verwendet werden.

Azure PowerShell ist auch in Azure [Cloud Shell](/azure/cloud-shell/overview) verfügbar und nun in [Docker-Images](azureps-in-docker.md) vorinstalliert.

## <a name="requirements"></a>Requirements (Anforderungen)

> [!NOTE]
> PowerShell 7.x und höher ist die für die Verwendung mit Azure PowerShell auf allen Plattformen empfohlene PowerShell-Version.

Azure PowerShell funktioniert mit PowerShell 6.2.4 und höher auf allen Plattformen. Es wird auch mit PowerShell 5.1 unter Windows unterstützt. Installieren Sie die [aktuelle PowerShell-Version](/powershell/scripting/install/installing-powershell) für Ihr Betriebssystem. Bei der Ausführung in PowerShell 6.2.4 und höher gibt es keine zusätzlichen Anforderungen an Azure PowerShell.

Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

So verwenden Sie Azure PowerShell in PowerShell 5.1 unter Windows:

1. Führen Sie ein Update auf [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus.
   Unter Windows 10, Version 1607 oder höher, ist PowerShell 5.1 bereits installiert.
2. Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).
3. Vergewissern Sie sich, dass die aktuelle Version von PowerShellGet installiert ist. Führen Sie `Install-Module -Name PowerShellGet -Force` aus.

## <a name="install-the-azure-powershell-module"></a>Installieren des Azure PowerShell-Moduls

> [!WARNING]
> Die Module AzureRM und Az können für PowerShell 5.1 unter Windows nicht gleichzeitig installiert sein. Wenn AzureRM weiterhin auf Ihrem System verfügbar sein soll, installieren Sie das Az-Modul für PowerShell 6.2.4 oder höher.

Die Verwendung der PowerShellGet-Cmdlets ist die bevorzugte Installationsmethode. Installieren Sie das Az-Modul nur für den aktuellen Benutzer. Dies ist der empfohlene Installationsbereich. Die Funktionsweise dieser Methode ist auf Windows-, macOS- und Linux-Plattformen gleich. Führen Sie den folgenden Befehl in einer PowerShell-Sitzung aus:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert. Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.

Zum Installieren des Moduls für alle Benutzer in einem System sind erhöhte Rechte erforderlich. Starten Sie unter Windows die PowerShell-Sitzung mithilfe der Option **Als Administrator ausführen**. Verwenden Sie unter macOS oder Linux den Befehl `sudo`:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Das Az-Modul ist ein Rollupmodul für die Azure PowerShell-Cmdlets. Wenn Sie es installieren, werden alle verfügbaren Azure PowerShell-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.

## <a name="install-offline"></a>Offlineinstallation

In einigen Umgebungen ist es nicht möglich, eine Verbindung mit dem PowerShell-Katalog herzustellen. In diesen Fällen können Sie die Installation mithilfe einer der folgenden Methoden weiterhin offline durchführen:

* Laden Sie die Module an einen anderen Speicherort in Ihrem Netzwerk herunter, und verwenden Sie diesen als Installationsquelle.
  Dieses Verfahren ermöglicht die Zwischenspeicherung von PowerShell-Modulen, die mithilfe von PowerShellGet auf Systemen ohne Verbindung bereitgestellt werden sollen, auf einem einzelnen Server oder in einer einzelnen Dateifreigabe. Unter [Arbeiten mit lokalen PowerShellGet-Repositorys](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) erfahren Sie, wie Sie ein lokales Repository einrichten und die Installation auf getrennten Systemen ausführen.
* [Laden Sie die Azure PowerShell MSI](install-az-ps-msi.md) auf einen mit dem Netzwerk verbundenen Computer herunter, und kopieren Sie anschließend das Installationsprogramm auf Systeme ohne Zugriff auf den PowerShell-Katalog. Beachten Sie, dass das MSI-Installationsprogramm nur für PowerShell 5.1 unter Windows verwendet werden kann.
* Speichern Sie das Modul mit [Save-Module](/powershell/module/PowershellGet/Save-Module) auf einer Dateifreigabe oder einer anderen Quelle, und kopieren Sie es manuell auf andere Computer:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Problembehandlung

In diesem Abschnitt finden Sie einige allgemeine Probleme, die bei der Installation des Azure PowerShell-Moduls auftreten können. Falls ein Problem auftritt, das hier nicht aufgeführt ist, [melden Sie es auf GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Der Proxy blockiert die Verbindung.

Wenn Sie von `Install-Module` Fehler erhalten, die anzeigen, dass der PowerShell-Katalog nicht erreichbar ist, befinden Sie sich möglicherweise hinter einem Proxy. Verschiedene Betriebssysteme und Netzwerkumgebungen haben unterschiedliche Anforderungen an die Konfiguration eines systemweiten Proxys. Wenden Sie sich an Ihren Systemadministrator, um Ihre Proxyeinstellungen zu erhalten und zu erfahren, wie Sie sie für Ihre Umgebung konfigurieren können.

PowerShell selbst ist möglicherweise nicht so konfiguriert, dass es diesen Proxy automatisch verwendet. Konfigurieren Sie bei PowerShell 5.1 und höher die PowerShell-Sitzung mit den folgenden Befehlen so, dass ein Proxy verwendet wird:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Wenn die Anmeldeinformationen Ihres Betriebssystems ordnungsgemäß konfiguriert sind, leitet diese Konfiguration PowerShell-Anforderungen über den Proxy weiter. Damit diese Einstellung auch zwischen den Sitzungen erhalten bleibt, fügen Sie die Befehle zu Ihrem [PowerShell-Profil](/powershell/module/microsoft.powershell.core/about/about_profiles) hinzu.

Ihr Proxy muss HTTPS-Verbindungen mit der folgenden Adresse zulassen, damit das Paket installiert werden kann:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Anmelden

Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Wenn Sie das automatische Laden von Modulen deaktiviert haben, importieren Sie das Modul manuell mit `Import-Module -Name Az`.
> Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.

Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualisieren des Azure PowerShell-Moduls

Zum Aktualisieren eines beliebigen PowerShell-Moduls müssen Sie dieselbe Methode verwenden, die zum Installieren des Moduls verwendet wurde. Wenn Sie beispielsweise ursprünglich `Install-Module` verwendet haben, müssen Sie [Update-Module](/powershell/module/powershellget/update-module) verwenden, um die neueste Version zu erhalten. Wenn Sie ursprünglich das MSI-Paket verwendet haben, müssen Sie das neue MSI-Paket herunterladen und installieren.

Die PowerShellGet-Cmdlets können keine Module aktualisieren, die über ein MSI-Paket installiert wurden. Mit MSI-Paketen werden keine Module aktualisiert, die mithilfe von PowerShellGet installiert wurden. Wenn bei der Aktualisierung mithilfe von PowerShellGet Probleme auftreten, sollten Sie eine **Neuinstallation** anstelle eines **Updates** durchführen. Die Neuinstallation erfolgt auf dieselbe Weise wie die Installation, Sie müssen jedoch den Parameter `-Force` hinzufügen:

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

Im Gegensatz zu MSI-basierten Installationen werden bei der Installation oder Aktualisierung mithilfe von PowerShellGet frühere Versionen nicht entfernt, die unter Umständen auf Ihrem System vorhanden sind. Wenn Sie frühere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md) weiter. Weitere Informationen zu MSI-basierten Installationen finden Sie unter [Installieren von Azure PowerShell mit einer MSI](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Verwenden von mehreren Versionen von Azure PowerShell

Es ist möglich, mehr als eine Version von Azure PowerShell zu installieren. Verwenden Sie den folgenden Befehl zum Überprüfen, ob Sie mehrere Versionen von Azure PowerShell installiert haben:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

Anweisungen zum Entfernen einer Version von Azure PowerShell finden Sie unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md).

Sind mehrere Versionen des Moduls installiert, wird mit der Funktion zum automatischen Laden von Modulen und mit `Import-Module` standardmäßig die neueste Version geladen.

Sie können eine bestimmte Version des `Az`-Moduls mithilfe des Parameters `-RequiredVersion` installieren oder laden:

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a>Verwenden mehrerer Repositorys mit PowerShellGet

Der Parameter **Repository** ist erforderlich, wenn Sie PowerShellGet auf Ihrem System zusätzliche Repositorys hinzugefügt haben und das Az-Modul in mehr als einem davon vorhanden ist.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a>Feedback geben

[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden. Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md). Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.
