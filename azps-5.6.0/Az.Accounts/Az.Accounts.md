---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 0c8773066f39d11e6985bbe4bd1f1e69cd9142f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938379"
---
# Az.Accounts-Modul
## Beschreibung
Verwaltet Anmeldeinformationen und allgemeine Konfiguration für alle Azure-Module.

## Az.Accounts-Cmdlets
### [Add-AzEnvironment](Add-AzEnvironment.md)
Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.

### [Clear-AzContext](Clear-AzContext.md)
Entfernen Sie alle Azure-Anmeldeinformationen, Konto- und Abonnementinformationen.

### [Clear-AzDefault](Clear-AzDefault.md)
Deaktiviert die vom Benutzer im aktuellen Kontext festgelegten Standardwerte.

### [Connect-AzAccount](Connect-AzAccount.md)
Stellen Sie eine Verbindung mit Azure mit einem authentifizierten Konto zur Verwendung mit Cmdlets aus den Az-PowerShell-Modulen bereit.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Deaktivieren Sie die automatische Speicherung von Azure-Anmeldeinformationen.  Ihre Anmeldeinformationen werden beim nächsten Öffnen eines PowerShell-Fensters vergessen

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Opts out of collecting data to improve the Azure PowerShell cmdlets. Die Daten werden standardmäßig erfasst, es sei denn, Sie melde sich explizit ab.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Deaktiviert AzureRm-Präfixaliase für Az-Module.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte, die diesem Konto zugeordnet sind.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Azure-Kontexte sind PowerShell-Objekte, die Ihr aktives Abonnement zum Ausführen von Befehlen darstellen, und die Authentifizierungsinformationen, die zum Herstellen einer Verbindung mit einer Azure-Cloud erforderlich sind. Bei Azure-Kontexten muss Azure PowerShell Ihr Konto nicht jedes Mal erneut authentifizieren, wenn Sie abonnements wechseln. Weitere Informationen finden Sie unter [Azure PowerShell-Kontextobjekte](https://docs.microsoft.com/powershell/azure/context-persistence).

Mit diesem Cmdlet können die Azure-Kontextinformationen gespeichert und automatisch geladen werden, wenn Sie einen PowerShell-Prozess starten. Beispielsweise beim Öffnen eines neuen Fensters.

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit den Azure PowerShell-Cmdlets zu verbessern. Beim Ausführen dieses Cmdlets wird die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer verwendet. Die Daten werden standardmäßig erfasst, es sei denn, Sie melde sich explizit ab.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Aktiviert AzureRm-Präfixaliase für Az-Module.

### [Get-AzAccessToken](Get-AzAccessToken.md)
Unformatiertes Zugriffstoken erhalten. Stellen Sie bei Verwendung von -ResourceUrl sicher, dass der Wert der aktuellen Azure-Umgebung zu entsprechen hat. Sie können auf den Wert von `(Get-AzContext).Environment` verweisen.

### [Get-AzContext](Get-AzContext.md)
Ruft die Metadaten ab, die zum Authentifizieren von Azure Resource Manager-Anforderungen verwendet werden.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Anzeigen von Metadaten zum automatischen Speichern des Kontextfeatures, einschließlich der Frage, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext- und Anmeldeinformationen gefunden werden können.

### [Get-AzDefault](Get-AzDefault.md)
Holen Sie sich die vom Benutzer im aktuellen Kontext festgelegten Standardwerte.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Holen Sie sich Endpunkte und Metadaten für eine Instanz von Azure-Diensten.

### [Get-AzSubscription](Get-AzSubscription.md)
Holen Sie sich Abonnements, auf die das aktuelle Konto zugreifen kann.

### [Get-AzTenant](Get-AzTenant.md)
Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.

### [Import-AzContext](Import-AzContext.md)
Lädt Azure-Authentifizierungsinformationen aus einer Datei.

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
Erstellen und Ausführen einer HTTP-Anforderung nur an Azure-Ressourcenverwaltungsendpunkt

### [Register-AzModule](Register-AzModule.md)
NUR FÜR INTERNE VERWENDUNG – Bereitstellen von Runtime-Unterstützung für generierte AutoRest-Cmdlets

### [Remove-AzContext](Remove-AzContext.md)
Entfernen eines Kontexts aus der Gruppe verfügbarer Kontexte

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Entfernt Endpunkte und Metadaten für die Verbindung mit einer bestimmten Azure-Instanz.

### [Rename-AzContext](Rename-AzContext.md)
Benennen Sie einen Azure-Kontext um.  Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.

### [Resolve-AzError](Resolve-AzError.md)
Zeigen Sie detaillierte Informationen zu PowerShell-Fehlern mit erweiterten Details für Azure PowerShell-Fehler an.

### [Save-AzContext](Save-AzContext.md)
Speichert die aktuellen Authentifizierungsinformationen für die Verwendung in anderen PowerShell-Sitzungen.

### [Select-AzContext](Select-AzContext.md)
Auswählen eines Abonnements und Kontos, das in Azure PowerShell-Cmdlets als Ziel verwendet werden soll

### [Senden von Feedback](Send-Feedback.md)
Sendet feedback an das Azure PowerShell-Team über eine Reihe von geführten Eingabeaufforderungen.

### [Set-AzContext](Set-AzContext.md)
Legt den Mandanten, das Abonnement und die Umgebung für cmdlets fest, die in der aktuellen Sitzung verwendet werden.

### [Set-AzDefault](Set-AzDefault.md)
Festlegen einer Standardeinstellung im aktuellen Kontext

### [Set-AzEnvironment](Set-AzEnvironment.md)
Legt Eigenschaften für eine Azure-Umgebung fest.

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
Entfernt alle AzureRm-Module von einem Computer.

