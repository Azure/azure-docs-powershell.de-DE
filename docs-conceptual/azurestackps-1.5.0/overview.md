---
title: Übersicht über Azure Stack PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053357"
---
# <a name="azure-stack-module-150"></a>Azure Stack-Modul 1.5.0

## <a name="requirements"></a>Anforderungen:
Die niedrigste unterstützte Azure Stack-Version ist 1808.

Hinweis: Falls Sie eine niedrigere Version verwenden, sollten Sie Version 1.4.0 installieren.

## <a name="known-issues"></a>Bekannte Probleme:

- Mit „New-AzsOffer“ können keine öffentlichen Angebote erstellt werden. Das Cmdlet „Set-AzsOffer“ muss hinterher aufgerufen werden, um den Zustand zu ändern.
- Ein IP-Pool kann nicht ohne erneute Bereitstellung entfernt werden.

## <a name="install"></a>Installieren
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>Versionsinformationen
* Alle Azure Stack-Module mit Administratorrechten werden auf eine Version aktualisiert, die höher oder gleich der Abhängigkeit vom AzureRm.Profile-Modul sind
* Unterstützung für die Verarbeitung von geschachtelten Ressourcennamen in allen Modulen
* Fehlerbehebung in allen Modulen, in denen „ErrorActionPreference“ außer Kraft gesetzt wird und „Stop“ lautet
* Azs.Compute.Admin-Modul
    * Neue Kontingenteigenschaften für die Unterstützung eines verwalteten Datenträgers hinzugefügt
    * Cmdlets für Datenträgermigration hinzugefügt
    * Zusätzliche Eigenschaften in Plattformimage und VM-Erweiterungsobjekten
* Azs.Fabric.Admin 
    * Neues Cmdlet zum Hinzufügen eines Skalierungseinheitknotens
* Azs.Backup.Admin
    * Set-AzsBackupShare ist ein Alias, jetzt Cmdlet Set-AzsBackupConfiguration
    * Get-AzsBackupLocation ist ein Alias, jetzt Cmdlet Get-AzsBackupConfiguration
    * Set-AzsBackupConfiguration, Parameter „BackupShare“ ist jetzt ein Alias für den Parameterpfad
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer, Parameter „OfferName“ ist jetzt ein Alias für „Offer“
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer, Parameter „OfferName“ ist jetzt ein Alias für „Offer“

## <a name="content"></a>Inhalt:
### <a name="azure-bridge"></a>Azure-Bridge
Vorschauversion des AzureBridge-Administratormoduls von Azure Stack, mit dem Sie Images aus Azure syndizieren können.

### <a name="backup"></a>Backup
Vorschauversion des Backup-Administratormoduls, das Administratoren Folgendes ermöglicht:
- Konfigurieren des Speicherorts von Sicherungen
- Durchführen von Sicherungen
- Auflisten und Wiederherstellen abgeschlossener Sicherungen

### <a name="commerce"></a>Commerce
Vorschauversion des Commerce-Administratormoduls von Azure Stack, mit dem die aggregierte Datennutzung für das gesamte Azure Stack-System angezeigt werden kann.

### <a name="compute"></a>Compute
Vorschauversion des Compute-Administratormoduls von Azure Stack mit Funktionen zur Verwaltung von Computekontingenten, Plattformimages, verwalteten Datenträgern und VM-Erweiterungen.

### <a name="fabric"></a>Fabric
Vorschauversion des Fabric-Administratormoduls von Azure Stack, mit dem Administratoren Infrastrukturkomponenten anzeigen und verwalten können:
- Beenden, Starten und Herunterfahren von Skalierungseinheitknoten
- Entladen und Fortsetzen von Skalierungseinheitknoten für FRU-bezogene Aktivitäten
- Reparieren von Skalierungseinheitknoten
- Neustarten der Infrastrukturrolle
- Beenden, Starten und Herunterfahren von Instanzen der Infrastrukturrolle
- Erstellen neuer IP-Pools


### <a name="gallery"></a>Galerie
Vorschauversion des Gallery-Administratormoduls von Azure Stack mit Funktionen zum Verwalten von Katalogelementen im Azure Stack-Marketplace.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Vorschauversion des Infrastructure Insights-Administratormoduls, das Administratoren Folgendes ermöglicht:
- Anzeigen der Integrität ihrer Azure Stack-Stempelressourcen
- Anzeigen und Verwalten von Warnungen

### <a name="keyvault"></a>KeyVault
Vorschauversion des KeyVault-Administratormoduls von Azure Stack, mit dem Administratoren KeyVault-Kontingente anzeigen können.

### <a name="network"></a>Netzwerk
Vorschauversion des Network-Administratormoduls, das Folgendes ermöglicht:
- Verwalten von Netzwerkkontingenten
- Anzeigen zugeordneter Netzwerkressourcen (beispielsweise öffentliche IP-Adressen, virtuelle Netzwerke oder Lastenausgleichsmodule)
- Stellt ein Cmdlet zum Anzeigen einer Administratorübersicht bereit.

### <a name="storage"></a>Storage
Vorschauversion des Storage-Administratormoduls von Azure Stack.  Dieses Release bietet Funktionen für Folgendes:
- Verwalten von Speicherkontingenten
- Durchführen der Garbage Collection für gelöschte Speicherressourcen
- Wiederherstellen gelöschter Speicherkonten
- Migrieren von Containern zwischen Freigaben
- Anzeigen von Informationen zu den einzelnen Speicherkomponenten
- Anzeigen von Nutzungs- und Leistungsinformationen

### <a name="subscription-admin"></a>Abonnementadministrator
Vorschauversion des Subscription-Administratormoduls von Azure Stack.  Dieses Modul bietet Administratorfunktionen für Folgendes:
- Verwalten von Plänen und Angeboten
- Anzeigen von Nutzungs- und Leistungsinformationen
- Verwalten der RBAC

### <a name="subscription"></a>Subscription
Vorschauversion des Subscription-Moduls von Azure Stack.  Dieses Modul bietet Benutzerfunktionen für Folgendes:
- Erstellen, Löschen und Aktualisieren von Abonnements

### <a name="update"></a>Aktualisieren
Vorschauversion des Update-Administratormoduls von Azure Stack.  Dieses Modul ermöglicht Administratoren Folgendes:
- Auflisten und Installieren verfügbarer Updates
- Fortsetzen unterbrochener Updates
- Anzeigen installierter Updates
