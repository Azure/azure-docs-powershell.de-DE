---
Module Name: Az.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
ms.openlocfilehash: ad8666a0524482521a5c1054ab46862ec6ce8dde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003966"
---
# AZ. ServiceBus-Modul
## Beschreibung
In diesem Thema werden Hilfethemen zu den Azure Service Bus-Cmdlets angezeigt.

## AZ. ServiceBus-Cmdlets
### [Vollständig – AzServiceBusMigration](Complete-AzServiceBusMigration.md)
Cmdlets setzen die Migration von Standard-zu Premium-Namespace als abgeschlossen fest, und Verbindungszeichenfolgen des Standardnamespace verweisen nun auf den Premium-Namespace.

### [Get-AzServiceBusAuthorizationRule](Get-AzServiceBusAuthorizationRule.md)
Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab. 

### [Get-AzServiceBusGeoDRConfiguration](Get-AzServiceBusGeoDRConfiguration.md)
Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab

### [Get-AzServiceBusKey](Get-AzServiceBusKey.md)
Ruft die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema oder den Alias (GeoDR-Konfigurationen) ab.

### [Get-AzServiceBusMigration](Get-AzServiceBusMigration.md)
Ruft MigrationConfiguration für den Namespace ab.

### [Get-AzServiceBusNamespace](Get-AzServiceBusNamespace.md)
Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.

### [Get-AzServiceBusOperation](Get-AzServiceBusOperation.md)
Liste unterstützter ServiceBus-Vorgänge

### [Get-AzServiceBusQueue](Get-AzServiceBusQueue.md)
Gibt eine Beschreibung für die angegebene ServiceBus-Warteschlange zurück.

### [Get-AzServiceBusRule](Get-AzServiceBusRule.md)
Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas. 

### [Get-AzServiceBusSubscription](Get-AzServiceBusSubscription.md)
Gibt eine Beschreibung des Abonnements für das angegebene Thema zurück.

### [Get-AzServiceBusTopic](Get-AzServiceBusTopic.md)
Gibt eine Beschreibung für das angegebene Service Bus-Thema zurück.

### [Neu – AzServiceBusAuthorizationRule](New-AzServiceBusAuthorizationRule.md)
Erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.

### [Neu – AzServiceBusAuthorizationRuleSASToken](New-AzServiceBusAuthorizationRuleSASToken.md)
Generiert eine SAS-tolen für Azure serviucebus-Autorisierungsregel für Namespace/Queue/Topic. 

### [Neu – AzServiceBusGeoDRConfiguration](New-AzServiceBusGeoDRConfiguration.md)
Erstellt einen neuen Alias (Disaster Recovery-Konfiguration)

### [Neu – AzServiceBusKey](New-AzServiceBusKey.md)
Generiert die primären oder sekundären Verbindungszeichenfolgen für den ServiceBus-Namespace oder die Warteschlange oder das Thema neu.

### [Neu – AzServiceBusNamespace](New-AzServiceBusNamespace.md)
Erstellt einen neuen ServiceBus-Namespace.

### [Neu – AzServiceBusQueue](New-AzServiceBusQueue.md)
Erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.

### [Neu – AzServiceBusRule](New-AzServiceBusRule.md)
Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas. 

### [Neu – AzServiceBusSubscription](New-AzServiceBusSubscription.md)
Erstellt ein Abonnement für das angegebene Service Bus-Thema.

### [Neu – AzServiceBusTopic](New-AzServiceBusTopic.md)
Erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.

### [Remove-AzServiceBusAuthorizationRule](Remove-AzServiceBusAuthorizationRule.md)
Entfernt die Autorisierungsregel für einen ServiceBus-Namespace oder eine Warteschlange oder ein Thema aus der angegebenen Ressourcengruppe.

### [Remove-AzServiceBusGeoDRConfiguration](Remove-AzServiceBusGeoDRConfiguration.md)
Löscht einen Alias (Disaster Recovery-Konfiguration)

### [Remove-AzServiceBusMigration](Remove-AzServiceBusMigration.md)
Cmdlet löscht die Migrations Konfiguration für Standard mäßige in Premium-Namespaces

### [Remove-AzServiceBusNamespace](Remove-AzServiceBusNamespace.md)
Entfernt den Namespace aus der angegebenen Ressourcengruppe. 

### [Remove-AzServiceBusQueue](Remove-AzServiceBusQueue.md)
Entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.

### [Remove-AzServiceBusRule](Remove-AzServiceBusRule.md)
Entfernt die angegebene Regel eines angegebenen Abonnements.

### [Remove-AzServiceBusSubscription](Remove-AzServiceBusSubscription.md)
Entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.

### [Remove-AzServiceBusTopic](Remove-AzServiceBusTopic.md)
Entfernt das Thema aus dem angegebenen ServiceBus-Namespace.

### [Satz-AzServiceBusAuthorizationRule](Set-AzServiceBusAuthorizationRule.md)
Aktualisiert die angegebene Autorisierungsregel Beschreibung für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.

### [Satz-AzServiceBusGeoDRConfigurationBreakPair](Set-AzServiceBusGeoDRConfigurationBreakPair.md)
Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.

### [Satz-AzServiceBusGeoDRConfigurationFailOver](Set-AzServiceBusGeoDRConfigurationFailOver.md)
Ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.

### [Satz-AzServiceBusNamespace](Set-AzServiceBusNamespace.md)
Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.

### [Satz-AzServiceBusQueue](Set-AzServiceBusQueue.md)
Aktualisiert die Beschreibung einer Service Bus-Warteschlange im angegebenen ServiceBus-Namespace.

### [Satz-AzServiceBusRule](Set-AzServiceBusRule.md)
Aktualisiert die angegebene Regelbeschreibung für das angegebene Abonnement.

### [Satz-AzServiceBusSubscription](Set-AzServiceBusSubscription.md)
Aktualisiert eine Abonnementbeschreibung für ein Service Bus-Thema im angegebenen ServiceBus-Namespace.

### [Satz-AzServiceBusTopic](Set-AzServiceBusTopic.md)
Aktualisiert die Beschreibung eines Service Bus-Themas im angegebenen ServiceBus-Namespace.

### [Anfang-AzServiceBusMigration](Start-AzServiceBusMigration.md)
Erstellt eine neue Migrations Konfiguration und startet die Migration von Entitäten von Standard-zu Premium-Namespaces

### [Stopp-AzServiceBusMigration](Stop-AzServiceBusMigration.md)
{{Füllen Sie die Zusammenfassung aus}}

### [Test-AzServiceBusName](Test-AzServiceBusName.md)
Überprüft die Verfügbarkeit des angegebenen Namespace namens oder-Alias (Dr-Konfigurationsname). 

