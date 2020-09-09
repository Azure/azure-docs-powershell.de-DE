---
title: Azure PowerShell-Änderungsprotokoll
description: Hierbei handelt es sich um einen Verlauf der Änderungen, die in der neuesten Version an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: e6dd28596cdc4f18ddcd3de7886d222ed588caff
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243666"
---
# <a name="azure-powershell-release-notes"></a>Versionshinweise zu Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Hierbei handelt es sich um eine Liste der Änderungen, die in dieser Version an Azure PowerShell vorgenommen wurden.

---

## <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Azure PowerShell 5.7.0-Installationsprogramm: [Link](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

Katalog-Modul für ARM-Cmdlets: [Link](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

Führen Sie zum Installieren von `AzureRM` aus dem PowerShell-Katalog den folgenden Befehl aus:

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

Führen Sie zum Aktualisieren von einer älteren Version von `AzureRM` den folgenden Befehl aus:

```powershell-interactive
Update-Module -Name AzureRM
```

### <a name="changes-since-last-release"></a>Änderungen seit der letzten Version

#### <a name="general"></a>Allgemein
* Aktualisiert auf die aktuelle Version von Azure ClientRuntime

#### <a name="azurestorage"></a>Azure.Storage
* Das Problem, dass beim Ausführen der Cmdlets zum Hochladen von Blobs und Dateien auf Computern mit aktivierter FIPS-Richtlinie auftrat, wurde behoben.
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* New Cmdlet Get-AzureRmEnrollmentAccount
  - Cmdlet zum Abrufen von Registrierungskonten

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integration in Cognitive Services Management SDK (Version 4.0.0)
* Vorgang „Get-AzureRmCognitiveServicesAccountUsage“ hinzugefügt

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus` unterstützt den Verschlüsselungsstatus auf Datenträgerebene
* `Get-AzureRmVmssVmDiskEncryptionStatus` unterstützt den Verschlüsselungsstatus auf Datenträgerebene
* Update für Zonenresilienz
* „New-AzureRmVm“ und „New-AzureRmVmss“ (einfacher Parametersatz) unterstützen Verfügbarkeitszonen.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Abhängigkeit von „Commands.Resources.Rest“ und ARM/Storage SDKs aufgehoben.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Funktionalität zum Debuggen hinzugefügt
* Version des ADLS Dataplane SDK auf 1.1.2 aktualisiert
* Export-AzureRmDataLakeStoreItem: Parameter „PerFileThreadCount“ und „ConcurrentFileCount“ als veraltet markiert, Parameter „Concurrency“ eingeführt
* Import-AzureRMDataLakeStoreItem: Parameter „PerFileThreadCount“ und „ConcurrentFileCount“ als veraltet markiert, Parameter „Concurrency“ eingeführt
* Get-AzureRMDataLakeStoreItemContent: Fragmentverhalten für Inhalte über 4 MB korrigiert
* Set-AzureRMDataLakeStoreItemExpiry: Neuer Parametersatz „SetRelativeExpiry“ zum Festlegen der relativen Ablaufzeit eingeführt
* Remove-AzureRmDataLakeStoreItem: Parameter „Clean“ als veraltet markiert.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* „AlternameName“ in „New-AzureRmEventHubGeoDRConfiguration“korrigiert

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Cmdlets zum Aufnehmen von Pipingszenarien
* Benachrichtigung über veraltete Elemente für anstehende Version mit grundlegenden Änderungen hinzugefügt

#### <a name="azurermnetwork"></a>AzureRM.Network
* Fehlermeldung mit Netzwerk-Cmdlets korrigiert

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* „properties“ in „CorrelationFilter“ von „Rules“ zur Unterstützung benutzerdefinierter Eigenschaften (customproperties) hinzugefügt
* Hilfe zu „New-AzureRmServiceBusGeoDRConfiguration“ aktualisiert und Ausgabe des Rules-Cmdlets korrigiert
* Eigenschaften für die automatische Weiterleitung im Cmdlet „New-AzureRmServiceBusQueue“ und „New-AzureRmServiceBusSubscription“ korrigiert

#### <a name="azurermsql"></a>AzureRM.Sql
* Neues Cmdlet „Stop-AzureRmSqlElasticPoolActivity“ hinzugefügt, um das Abbrechen der asynchronen Vorgänge für Pools für elastische Datenbanken zu unterstützen
* Die Antwort für die Cmdlets „Get-AzureRmSqlDatabaseActivity“ und „Get-AzureRmSqlElasticPoolActivity“ wurde aktualisiert, damit die Antwort mehr Informationen enthalten kann.

Änderungen seit der letzten Version: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 – März 2018

#### <a name="general"></a>Allgemein
* Problem mit Standardressourcengruppe in CloudShell behoben
* Problem mit falschen Startskripts behoben, die während des Modulimports ausgeführt wurden

#### <a name="azurermprofile"></a>AzureRM.Profile
* MSI-Authentifizierung in nicht unterstützten Szenarien aktiviert
* Unterstützung für benutzerdefinierte verwaltete Dienstidentität hinzugefügt

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Problem mit dem Bereinigen von Skripts in Builds behoben

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Problem mit dem Bereinigen von Skripts in Builds behoben

#### <a name="azurermcompute"></a>AzureRM.Compute
* „New-AzureRmVM“ und „New-AzureRmVMSS“ unterstützen Datenträger.
* „New-AzureRmVM“ und „New-AzureRmVMSS“ unterstützen benutzerdefinierte Images nach Name oder ID.
* Protokollanalysefunktion
    - Cmdlet „Export-AzureRmLogAnalyticRequestRateByInterval“ hinzugefügt
    - Cmdlet „Export-AzureRmLogAnalyticThrottledRequests“ hinzugefügt

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Problem mit Parametersätzen für Containerregistrierung und Azure-Dateivolumebindung behoben

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF-.Net SDK auf Vorschauversion 0.6.0 mit den folgenden Änderungen aktualisiert:
    - Neuer verknüpfter Dienst „AzureDatabricks“ und Aktivität „DatabricksNotebook“ hinzugefügt
    - Eigenschaften „headNodeSize“ und „dataNodeSize“ im verknüpften Dienste „HDInsightOnDemand“ hinzugefügt
    - „LinkedService“, „Dataset“, „CopySource“ für „SalesforceMarketingCloud“ hinzugefügt
    - Unterstützung für „SecureOutput“ für alle Aktivitäten hinzugefügt
    - Neue BatchCount-Eigenschaft zu ForEach-Aktivität hinzugefügt, welche die Anzahl der gleichzeitig ausgeführten Aktivitäten steuert
    - Neue Filteraktivität hinzugefügt
    - Unterstützung für Parameter von verknüpften Diensten hinzugefügt

#### <a name="azurermdns"></a>AzureRM.Dns
* Unterstützung für private DNS-Zonen (öffentliche Vorschau)
    - Möglichkeit zum Erstellen von DNS-Zonen hinzugefügt, die nur für die zugewiesenen virtuellen Netzwerke sichtbar sind

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aktualisierung der Modelltypen für die Kompatibilität mit DNS-Cmdlets.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Änderungen für ASR Azure zu Azure Site Recovery (Cmdlets unterstützen derzeit Vorgänge für Unternehmen zu Unternehmen, Unternehmen zu Azure, HyperV zu Azure, VMware zu Azure)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Die folgenden Parameter in neuen und festgelegten Speicherkonto-Cmdlets sind veraltet: „EnableEncryptionService“ und „DisableEncryptionService“, da die Verschlüsselung ruhender Daten standardmäßig aktiviert ist und nicht deaktiviert werden kann.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Hilfe für „Remove-AzureRmWebAppSlot“ korrigiert

## <a name="550---march-2018"></a>5.5.0: März 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Problem mit dem Import von Aliasen behoben
* Paralleles Laden von Version 10.0.3 von Newtonsoft.Json und Version 6.0.8

#### <a name="azurestorage"></a>Azure.Storage
* Unterstützung des Features für vorläufiges Löschen
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Problem mit dem Import von Aliasen behoben
* Unterstützung der Firewall und des Features für die horizontale Skalierung von Abfragen sowie Unterstützung der API-Version 2017-08-01 hinzugefügt

#### <a name="azurermautomation"></a>AzureRM.Automation
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* „notice.txt“ und and Hinweismeldung aktualisiert

#### <a name="azurermcompute"></a>AzureRM.Compute
* „New-AzureRmVMSS“ gibt Verbindungszeichenfolgen im ausführlichen Modus aus.
* „New-AzureRmVmss“ unterstützt öffentliche IP-Adressen, Lastenausgleichsregeln und eingehende NAT-Regeln.
* WriteAccelerator-Feature
    - Den folgenden Cmdlets wurde der Switch-Parameter „WriteAccelerator“ hinzugefügt: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - Dem folgenden Cmdlet wurde der Switch-Parameter „OsDiskWriteAccelerator“ hinzugefügt:     Set-AzureRmVmssStorageProfile.
    - Den folgenden Cmdlets wurde der boolesche Parameter „OsDiskWriteAccelerator“ hinzugefügt:     Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Das Problem bei der Verschlüsselung von Anmeldeinformationen, das keinen sinnvollen Fehler bei einigen Verschlüsselungsvorgängen verursachte, wurde behoben.
* Integration Runtime kann nun in der gesamten Data Factory freigegeben werden.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Parameter „SetupScriptContainerSasUri“ und „Edition“ für das Cmdlet „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Funktionen zur benutzerdefinierten Einrichtung und Editionsauswahl zu aktivieren
* Das Problem bei der Verschlüsselung von Anmeldeinformationen, das keinen sinnvollen Fehler bei einigen Verschlüsselungsvorgängen verursachte, wurde behoben.
* Integration Runtime kann nun in der gesamten Data Factory freigegeben werden.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Beispiel für „Set-AzureRmKeyVaultAccessPolicy“ korrigiert

#### <a name="azurermnetwork"></a>AzureRM.Network
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermresources"></a>AzureRM.Resources
* Problem mit dem Import von Aliasen behoben

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Eigenschaft „EnableBatchedOperations“ zur Warteschlange hinzugefügt
* Eigenschaft „DeadLetteringOnFilterEvaluationExceptions“ zu Abonnements hinzugefügt

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Aktualisierung des Service Fabric-Cmdlets
  - ARM-Vorlagen aktualisiert
  - Für fehlerhafte Vorgänge wird kein Rollback mehr ausgeführt.
  - Add-AzureRmServiceFabricNodeType
    - Für virtuelle Computer werden standardmäßig verwaltete Datenträger festgelegt.
    - Vorhandenes VMSS-Subnetz wird verwendet.
    - Alle Vorgänge sind idempotent.
  - „Remove-AzureRmServiceFabricNodeType“ bereinigt teilweise erstellte VMSS und/oder Clusterknotentypen.
  - Ausgabe des PSCluster-Objekts für komplexe Eigenschaftstypen korrigiert

#### <a name="azurermsql"></a>AzureRM.Sql
* Problem mit dem Import von Aliasen behoben
* Die Antwort von „Get-AzureRmSqlServer“, „New-AzureRmSqlServer“ und „Remove-AzureRmSqlServer“ enthält nun die FullyQualifiedDomainName-Eigenschaft.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Problem mit dem Import von Aliasen behoben
* New-AzureRMWebApp: Parameter für vereinfachte WebApp-Erstellung mit Unterstützung von lokalen Git-Repository hinzugefügt

## <a name="540---february-2018"></a>5.4.0: Februar 2018
#### <a name="azurermautomation"></a>AzureRM.Automation
* Der Alias von „New-AzureRmAutomationModule“ wurde zu „Import-AzureRmAutomationModule“ hinzugefügt.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Das ErrorAction-Problem wurde für einige Get-Cmdlets behoben.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Azure-Containerinstanz-SDK 2018-02-01 wird angewendet.
    - Unterstützung der DNS-Namensbezeichnung

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Alle GET-Cmdlets, die zuvor nicht funktioniert haben, wurden korrigiert.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Korrektur eines Fehlers in der Hilfe zu „Get-AzureRmEventHubGeoDRConfiguration“

#### <a name="azurermnetwork"></a>AzureRM.Network
* Cmdlet zum Erstellen eines neuen Verbindungsmonitors hinzugefügt
    - New-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet zum Aktualisieren eines Verbindungsmonitors hinzugefügt
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet zum Abrufen des Verbindungsmonitors oder der Verbindungsmonitorliste hinzugefügt
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet zum Abfragen eines Verbindungsmonitors hinzugefügt
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Cmdlet zum Starten eines Verbindungsmonitors hinzugefügt
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet zum Beenden eines Verbindungsmonitors hinzugefügt
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet zum Entfernen eines Verbindungsmonitors hinzugefügt
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Die Dokumentation zu „Set-AzureRmApplicationGatewayBackendAddressPool“ wurde aktualisiert, und dabei wurde ein veraltetes Beispiel entfernt.
* EnableHttp2-Flag zu Application Gateway hinzugefügt
    - „New-AzureRmApplicationGateway“ wurde aktualisiert: Optionaler Parameter „-EnableHttp2“ hinzugefügt
* „IpTags“ zu „PublicIpAddress“ hinzugefügt
    - „New-AzureRmPublicIpAddress“ wurde aktualisiert: „IpTags“ hinzugefügt
    - „New-AzureRmPublicIpTag“ zum Hinzufügen von „Iptag“
* Eigenschaft „DisableBgpRoutePropagation“ in „RouteTable“ und „effectiveRoute“ hinzugefügt.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature: Fehlendes Beispiel in den Dokumenten hinzugefügt
* Register-AzureRmResourceProvider: Fehlendes Beispiel in den Dokumenten hinzugefügt

#### <a name="azurermstorage"></a>AzureRM.Storage
* Die folgenden Parameter in neuen und festgelegten Speicherkonto-Cmdlets sind veraltet: „EnableEncryptionService“ und „DisableEncryptionService“, da die Verschlüsselung ruhender Daten standardmäßig aktiviert ist und nicht deaktiviert werden kann.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0: Februar 2018
### <a name="azurermprofile"></a>AzureRM.Profile
* Warnung zur Einstellung von PowerShell 3 und 4 hinzugefügt
* `Add-AzureRmAccount` wurde in `Connect-AzureRmAccount` umbenannt. Für den alten Cmdlet-Namen wurde ein Alias hinzugefügt, und andere Aliase (`Login-AzAccount` und `Login-AzureRmAccount`) wurden zum neuen Cmdlet-Namen umgeleitet.
* `Remove-AzureRmAccount` wurde in `Disconnect-AzureRmAccount` umbenannt. Für den alten Cmdlet-Namen wurde ein Alias hinzugefügt, und andere Aliase (`Logout-AzAccount` und `Logout-AzureRmAccount`) wurden zum neuen Cmdlet-Namen umgeleitet.
* Ressourcenzeichenfolgen wurden korrigiert und verwenden nun `Connect-AzureRmAccount` anstelle von `Login-AzureRmAccount`.
* `Add-AzureRmEnvironment` und `Set-AzureRmEnvironment`
  - `-AzureOperationalInsightsEndpoint` und `-AzureOperationalInsightsEndpointResourceId` wurden als Parameter für die Verwendung mit der OperationalInsights-Datenebene (vertrauende Seite) hinzugefügt.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.

### <a name="azurermcompute"></a>AzureRM.Compute
* Der Parameter `-AvailabilitySetName` wurde zum vereinfachten Parametersatz von `New-AzureRmVM` hinzugefügt.
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.
* Benutzern wurde Identitätsunterstützung für virtuelle Computer und VM-Skalierungsgruppen hinzugefügt.
    - Die Parameter `-IdentityType` und `-IdentityId` werden zu `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` und `Update-AzureRmVmss` hinzugefügt.
* Parameter `-EnableIPForwarding` zu `Add-AzureRmVmssNetworkInterfaceConfig` hinzugefügt
* Parameter `-Priority` zu `New-AzureRmVmssConfig` hinzugefügt

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.
* Die Fehlermeldung von `Test-AzureRmDataLakeStoreAccount` wurde korrigiert, wenn dieses Cmdlet ohne Anmeldung mit `Login-AzureRmAccount` ausgeführt wird.

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Wurde aktualisiert, sodass die API-Version 2018-01-01 verwendet wird.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* Die folgenden neuen Befehle wurden für Notfallwiederherstellungsvorgänge mit Georeplikation hinzugefügt:
  - Erstellen einen neuen Alias (Konfiguration für Notfallwiederherstellung):
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Abrufen des Alias (Konfiguration für Notfallwiederherstellung):
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Deaktivieren der Notfallwiederherstellung und Beenden der Replikation von Änderungen vom primären Namespace zu sekundären Namespaces
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Auslösen eines Notfallwiederherstellungsfailovers und Neukonfiguration des Alias, um auf den sekundären Namespace zu zeigen
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Löschen eines Alias (Konfiguration für Notfallwiederherstellung)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* Die folgenden neuen Befehle wurden zum Überprüfen der Verfügbarkeit des Alias für den Namespacenamen und den Namen der Notfallwiederherstellungskonfiguration mit Georeplikation hinzugefügt.
  - Überprüfen der Verfügbarkeit des Namespace- oder Aliasnamens (Konfiguration für Notfallwiederherstellung):
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.

### <a name="azurermnetwork"></a>AzureRM.Network
* Die Überschreibungsmeldung „Are you sure you want to overwriteresource“ (Soll die Ressource überschrieben werden?) wurde korrigiert.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Unterstützung für V2-API-Abfragen über `Invoke-AzureRmOperationalInsightsQuery` wurde hinzugefügt. Weitere Informationen zur neuen API finden Sie unter [https://dev.loganalytics.io/](https://dev.loganalytics.io/).

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: `-ServicePrincipalName` wurde aus dem Standardparameterset „Empty“ entfernt, da es in Verbindung mit dem SPN-Parametersatz redundant war.

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* Funktionskorrektur für `Remove-AzureRmServiceBusRule` und `Get-AzureRmServiceBusKey` hinzugefügt.
* Die folgenden neuen Commandlets wurden für Notfallwiederherstellungsvorgänge mit Georeplikation hinzugefügt:
  - Erstellen einen neuen Alias (Konfiguration für Notfallwiederherstellung):
    - `New-AzureRmServiceBusDRConfigurations`
  - Abrufen des Alias (Konfiguration für Notfallwiederherstellung):
    - `Get-AzureRmServiceBusDRConfigurations`
  - Deaktivieren der Notfallwiederherstellung und Beenden der Replikation von Änderungen vom primären Namespace zu sekundären Namespaces
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Auslösen eines Notfallwiederherstellungsfailovers und Neukonfiguration des Alias, um auf den sekundären Namespace zu zeigen
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Löschen eines Alias (Konfiguration für Notfallwiederherstellung)
    - `Remove-AzureRmServiceBusDRConfigurations`
* `Test-AzureRmServiceBusName`-Commandlets wurden aktualisiert, um Vorgänge zum Überprüfen der Verfügbarkeit von Aliasnamen für Notfallwiederherstellung mit Georeplikation zu unterstützen.
  - Überprüfen der Verfügbarkeit des Namespace- oder Aliasnamens (Konfiguration für Notfallwiederherstellung):
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Die Verwendung von `Login-AzureRmAccount` wurde korrigiert, und es wird nun `Connect-AzureRmAccount` verwendet.

## <a name="520---january-2018"></a>5.2.0 – Januar 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Add-AzureRmAccount
  * MSI-Anmeldung für die Authentifizierung mit den Anmeldeinformationen der verwalteten Dienstidentität des aktuellen virtuellen Computers/Diensts hinzugefügt
  * KeyVault-Authentifizierung beim Anmelden mit vom Benutzer angegebenen Zugriffstoken korrigiert

#### <a name="azurestorage"></a>Azure.Storage
* Cmdlets zum Abrufen und Festlegen von Storage-Diensteigenschaften hinzugefügt
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmApiManagementProperty“, „Set-AzureRmApiManagementProperty“ und „New-AzureRmApiManagement“ wird nun „-Tag“ verwendet.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermautomation"></a>AzureRM.Automation
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „Set-AzureRmAutomationRunbook“ wird nun „-Tag“ verwendet.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermbatch"></a>AzureRM.Batch
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmCdnEndpoint“ und „New-AzureRmCdnProfile“ wird nun „-Tag“ verwendet.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integration in Cognitive Services Management SDK (Version 3.0.0)

#### <a name="azurermcompute"></a>AzureRM.Compute
* Vereinfachten Parametersatz zu „New-AzureRmVmss“ hinzugefügt, der eine VM-Skalierungsgruppe und alle erforderlichen Ressourcen mit intelligenten Standardwerten erstellt
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmVm“ und „Update-AzureRmVm“ wird nun „-Tag“ verwendet.
* Cmdlet „Get-AzureRmComputeResourceSku“ korrigiert, wenn „Zone“ in die Einschränkung einbezogen wird.
* Diagnose-Agent-Konfigurationsschema für Azure Monitor-Senkenunterstützung aktualisiert.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Azure Key Vault-Unterstützung für alle verknüpften Datenspeicherdienste aktiviert
* Lizenztypeigenschaft für Azure SSIS Integration Runtime hinzugefügt
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmDataFactory“ wird nun „-Tag“ verwendet.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Azure Key Vault-Unterstützung für alle verknüpften Datenspeicherdienste aktiviert
* Lizenztypeigenschaft für Azure SSIS Integration Runtime hinzugefügt
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Parameter „LicenseType“ für den Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Verwendung von AHUB-Funktionen zu ermöglichen

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmDataLakeAnalyticsAccount“ und „Set-AzureRmDataLakeAnalyticsAccount“ wird nun „-Tag“ verwendet.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmDataLakeStoreAccount“ und „Set-AzureRmDataLakeStoreAccount“ wird nun „-Tag“ verwendet.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermdns"></a>AzureRM.Dns
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Neues Cmdlet hinzugefügt:
  - Update-AzureRmEventGridSubscription
    - Dient zum Aktualisieren der Eigenschaften eines Event Grid-Ereignisabonnements.
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurerminsights"></a>AzureRM.Insights
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Zertifikatunterstützung für IoTHub-Cmdlets hinzugefügt
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Unterstützung von „-AsJob“ für KeyVault-Cmdlets mit langer Ausführungsdauer hinzugefügt. Ausgewählte Cmdlets können im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben.
  * Betroffenes Cmdlet: Remove-AzureRmKeyVault
* Fehler in „Set-AzureRmKeyVaultAccessPolicy“ behoben, durch den der AAD-Filter nicht den UPN, sondern den SPN auf den angegebenen UPN festgelegt hat
  - Weitere Informationen finden Sie im folgenden Artikel zum Problem: https://github.com/Azure/azure-powershell/issues/5201.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „Update-AzureRmMlCommitmentPlan“ wird nun „-Tag“ verwendet.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Parameter „IncludeAllResources“ zum Cmdlet „Remove-AzureRmMlOpCluster“ hinzugefügt
  - Durch Verwendung dieses Switch-Parameters werden alle Ressourcen entfernt, die ursprünglich zusammen mit dem Cluster erstellt wurden.
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermmedia"></a>AzureRM.Media
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „Set-AzureRmMediaService“ und „New-AzureRmMediaService“ wird nun „-Tag“ verwendet.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Unterstützung von „-AsJob“ für Network-Cmdlets mit langer Ausführungsdauer hinzugefügt. Ausgewählte Cmdlets können im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben.
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmNotificationHubsNamespace“ und „Set-AzureRmNotificationHubsNamespace“ wird nun „-Tag“ verwendet.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmOperationalInsightsSavedSearch“, „Set-AzureRmOperationalInsightsSavedSearch“, „New-AzureRmOperationalInsightsWorkspace“ und „Set-AzureRmOperationalInsightsWorkspace“ wird nun „-Tag“ verwendet.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Option „-UseOriginalStorageAccount“ zum Cmdlet „Restore-AzureRmRecoveryServicesBackupItem“ hinzugefügt.
  - Bei Verwendung dieses Flags werden Datenträger in ihren ursprünglichen Speicherkonten wiederhergestellt. Dadurch können Benutzer erreichen, dass die Konfiguration wiederhergestellter virtueller Computer möglichst exakt der Konfiguration der ursprünglichen virtuellen Computer entspricht.
  - Darüber hinaus verbessert sich dadurch die Leistung des Wiederherstellungsvorgangs.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Drei neue Cmdlets für Firewallregeln hinzugefügt
* Drei neue Cmdlets für die Georeplikation hinzugefügt
* Unterstützung für Zonen und Tags hinzugefügt
* „ResourceGroup“ optional, wann immer möglich

#### <a name="azurermrelay"></a>AzureRM.Relay
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermresources"></a>AzureRM.Resources
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Unterstützung von „-AsJob“ für Resources-Cmdlets mit langer Ausführungsdauer hinzugefügt. Ausgewählte Cmdlets können im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben.
* Alias aus „Get-AzureRmProviderOperation“ zu „Get-AzureRmResourceProviderAction“ hinzugefügt, um Namenskonventionen gerecht zu werden

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* „-Tags“ ist veraltet. Für „New-AzureRmServerManagementNode“ und „New-AzureRmServerManagementGateway“ wird nun „-Tag“ verwendet.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermsql"></a>AzureRM.Sql
* Beschreibung für Überwachungsbefehlsparameter aktualisiert
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Parameter „-AsJob“ zu Cmdlets mit langer Ausführungsdauer hinzugefügt
* Parameter „-DatabaseName“ von „Get-AzureRmSqlServiceObjective“ ausgemustert

#### <a name="azurermstorage"></a>AzureRM.Storage
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Nullverweisproblem beim Ausführen des Cmdlets „New-AzureRMStorageAccount“ mit dem Parameter „-EnableEncryptionService None“ behoben
* -AsJob-Unterstützung wurde für Storage-Cmdlets mit langer Ausführungsdauer hinzugefügt. Ausgewählte Cmdlets können im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben.
    - Betroffene Cmdlets: „New-“, „Remove-“, „Add-“ und „Update-“ für Speicherkonto und Speicherkonto-Netzwerkregel.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Ortsvervollständigung für Parameter vom Typ „-Location“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage gültiger Orte zu ermöglichen
* ResourceGroup-Vervollständigung für Parameter vom Typ „-ResourceGroup“ hinzugefügt, um die Vervollständigung mittels TAB-TASTE auf der Grundlage von Ressourcengruppen im aktuellen Abonnement zu ermöglichen
* Unterstützung von „-AsJob“ für Websites-Cmdlets mit langer Ausführungsdauer hinzugefügt. Ausgewählte Cmdlets können im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben.
     - Betroffene Cmdlets: „New-“, „Remove-“, „Add-“ und „Set-“ für „WebApps“, „AppServicePlan“ und „Slots“

## <a name="2017128-version-511"></a>2017.12.8 Version 5.1.1
* AnalysisServices
  - Der Validierungssatz des Speicherorts für die dynamische Suche wurde geändert, sodass alle Clouds unterstützt werden.
* Automation
  - Aktualisierung von Import-AzureRMAutomationRunbook
    - Unterstützung wird jetzt für Python2-Runbooks bereitgestellt.
* Batch
  - Ein Fehler wurde behoben, bei dem das automatische Erkennen der Ressourcengruppe für Kontovorgänge ohne eine Ressourcengruppe fehlgeschlagen ist.
* Compute
  - Get-AzureRmComputeResourceSku zeigt Zoneninformationen an.
  - „Disable-AzureRmVmssDiskEncryption“ aktualisiert, um das Problem zu beheben: https://github.com/Azure/azure-powershell/issues/5038
  - -AsJob-Unterstützung wurde für Compute-Cmdlets mit langer Ausführungsdauer hinzugefügt. Ausgewählte Cmdlets können im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben.
    - Betroffene Cmdlets: Cmdlets „New-“, „Update-“, „Set-“, „Remove-“, „Start-“, „Restart-“, „Stop-“ für Virtual Machines und VM-Skalierungsgruppen
    - Ein vereinfachter Parametersatz wurde zu New-AzureRmVM hinzugefügt, der einen virtuellen Computer und alle erforderlichen Ressourcen mithilfe intelligenter Standardwerte erstellt.
* ContainerInstance
  - Azure-Containerinstanz-SDK 2017-10-01 wird angewendet.
    - Unterstützung der Containerausführung bis zum Abschluss
    - Unterstützung für Azure-Dateivolumebindung
    - Unterstützung für das Öffnen mehrerer Ports für die öffentliche IP-Adresse
* ContainerRegistry
  - Neue Cmdlets für die Georeplikation und Webhooks
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - Die Funktion zum Verschlüsseln von Anmeldeinformationen funktioniert jetzt sowohl bei aktiviertem (über das Netzwerk) als auch bei deaktiviertem Remotezugriff (lokaler Computer).
* DataFactoryV2
  - Zwei neue Cmdlets wurden hinzugefügt: „Update-AzureRmDataFactoryV2“ und „Stop-AzureRmDataFactoryV2PipelineRun“
* DataLakeAnalytics
  - Ein Parameter namens ScriptParameter wurde zu Submit-AzureRmDataLakeAnalyticsJob hinzugefügt.
    - Ausführliche Informationen zu ScriptParameter finden Sie mit Get-Help zu Submit-AzureRmDataLakeAnalyticsJob.
  - Für New-AzureRmDataLakeAnalyticsAccount wurde der Parameter MaxDegreeOfParallelism in MaxAnalyticsUnits geändert.
    - Für den Parameter „MaxAnalyticsUnits“ wurde ein Alias hinzugefügt: MaxDegreeOfParallelism
  - Für New-AzureRmDataLakeAnalyticsComputePolicy wurde der Parameter MaxDegreeOfParallelismPerJob in MaxAnalyticsUnitsPerJob geändert.
    - Für den Parameter „MaxAnalyticsUnitsPerJob“ wurde ein Alias hinzugefügt: MaxDegreeOfParallelismPerJob
  - Für Set-AzureRmDataLakeAnalyticsAccount wurde der Parameter MaxDegreeOfParallelism in MaxAnalyticsUnits geändert.
    - Für den Parameter „MaxAnalyticsUnits“ wurde ein Alias hinzugefügt: MaxDegreeOfParallelism
  - Für Submit-AzureRmDataLakeAnalyticsJob wurde der Parameter DegreeOfParallelism in AnalyticsUnits geändert.
    - Für den Parameter „AnalyticsUnits“ wurde ein Alias hinzugefügt: DegreeOfParallelism
  - Für Update-AzureRmDataLakeAnalyticsComputePolicy wurde der Parameter MaxDegreeOfParallelismPerJob in MaxAnalyticsUnitsPerJob geändert.
    - Für den Parameter „MaxAnalyticsUnitsPerJob“ wurde ein Alias hinzugefügt: MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - Set-AzureRmMlOpCluster wurde hinzugefügt.
    - Aktualisiert die Clusteragentanzahl oder SSL-Konfiguration.
  - Orchestratoreigenschaften sind optional.
    - Der Dienst erstellt einen Dienstprinzipal, sofern keiner angegeben ist, sodass die Orchestratoreigenschaften jetzt optional sind.
* PowerBIEmbedded
  - Unterstützung für Power BI Embedded-Kapazitäts-Cmdlets wurde hinzugefügt.
  - Neues Cmdlet Get-AzureRmPowerBIEmbeddedCapacity – ruft die Details einer PowerBI Embedded-Kapazität ab.
  - Neues Cmdlet New-AzureRmPowerBIEmbeddedCapacity – erstellt eine neue PowerBI Embedded-Kapazität.
  - Neues Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity – löscht eine Instanz der PowerBI Embedded-Kapazität.
  - Neues Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity – setzt eine Instanz der PowerBI Embedded-Kapazität fort.
  - Neues Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity – hält eine Instanz der PowerBI Embedded-Kapazität an.
  - Neues Cmdlet Test-AzureRmPowerBIEmbeddedCapacity – testet das Vorhandensein einer Instanz der PowerBI Embedded-Kapazität.
  - Neues Cmdlet Update-AzureRmPowerBIEmbeddedCapacity – verändert eine Instanz der PowerBI Embedded-Kapazität.
* Profil
  - „USGovernmentActiveDirectoryEndpoint“ aktualisiert auf https://login.microsoftonline.us/
    - Weitere Informationen zu den Azure Government-Endpunktzuordnungen finden Sie im folgenden Artikel: https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - -AsJob-Unterstützung für Cmdlets wurde hinzugefügt, wodurch bestimmte Cmdlets im Hintergrund ausgeführt werden und einen Auftrag zum Nachverfolgen und Kontrollieren des Fortschritts zurückgeben können.
    - Der Parameter -AsJob wurde zum Cmdlet Get-AzureRmSubscription hinzugefügt.
* RecoveryServices.Backup
  - Ein Fehler wurde behoben – Get-AzureRmRecoveryServicesBackupItem muss einen Vergleich für den Containernamenfilter ausführen, bei dem die Groß- und Kleinschreibung nicht beachtet wird.
  - Ein Fehler wurde behoben  – AzureVmItem verfügt jetzt über eine Eigenschaft, die anzeigt, wann das letzte Mal ein Sicherungsvorgang ausgeführt wurde: LastBackupTime.
* Ressourcen
  - Ein Fehler wurde behoben, bei dem Get-AzureRMRoleAssignment zu einer Zuweisung ohne einen Rollendefinitionsnamen für benutzerdefinierte Rollen führt.
    - Benutzer können jetzt Get-AzureRMRoleAssignment mit Zuweisungen mit Rollendefinitionsnamen verwenden, unabhängig vom Typ der Rolle.
  - Ein Fehler wurde behoben, bei dem Set-AzureRMRoleRoleDefinition einen Fehler ausgegeben hat (RD nicht gefunden), wenn assignablescopes einen neuen Bereich enthielt.
    - Benutzer können jetzt Set-AzureRMRoleRoleDefinition mit zuweisbaren Bereichen, einschließlich neuer Bereiche, unabhängig von der Position des Bereichs verwenden.
  - Bereiche, die mit „/“ enden, sind zulässig.
    - Benutzer können jetzt die Commandlets RoleDefinition und RoleAssignment mit Bereichen verwenden, die mit „/“ enden, konsistent mit der API und CLI.
  - Benutzer dürfen RoleAssignment mithilfe des Delegierungsflags erstellen.
    - Benutzer können jetzt New-AzureRMRoleAssignment mit einer Option zum Hinzufügen des Delegierungsflags verwenden.
  - RoleAssignment wurde korrigiert, sodass die Bereichsparameter respektiert werden.
  - Ein Alias für ServicePrincipalName wurde im Cmdlet New-AzureRmRoleAssignment hinzugefügt.
    - Benutzer können jetzt ApplicationId anstelle von ServicePrincipalName verwenden, wenn sie das Commandlet New-AzureRmRoleAssignment verwenden.
* SiteRecovery
  - Warnungen für veraltete Befehle wurden für alle Cmdlets in diesem Modul hinzugefügt als Vorbereitung für die nächste Version mit grundlegenden Änderungen.
    - Im Leitfaden zu anstehenden grundlegenden Änderungen finden Sie weitere Informationen dazu, wie Sie Ihre Cmdlets aus AzureRM migrieren können.
* Sql
  - Die Möglichkeit zum Umbenennen einer Datenbank mithilfe von Set-AzureRmSqlDatabase wurde hinzugefügt.
  - Problem https://github.com/Azure/azure-powershell/issues/4974 behoben
    - Das Angeben eines ungültigen AUDIT_CHANGED_GROUP-Werts für Cmdlets zur Überwachung führt zu keinem Fehler mehr, dies wird in der nächsten Version entfernt.
  - Problem https://github.com/Azure/azure-powershell/issues/5046 behoben
    - Der AuditAction-Parameter in Cmdlets zur Überwachung wird nicht mehr ignoriert.
  - Ein Fehler wurde in Cmdlets zur Überwachung behoben, wenn der StorageKeyType „Secondary“ angegeben wird.
    - Beim Festlegen der BLOB-Überwachung wurde der primäre Speicherkontoschlüssel verwendet anstelle des sekundären Schlüssels unter Angabe des Werts „Secondary“ für den Parameter StorageKeyType.
  - Die Formulierung für die Bestätigungsmeldung von Set-AzureRmSqlServerTransparentDataEncryptionProtector wurde geändert.
* Azure (RDFE)
    - Alle RemoteApp-Cmdlets wurden entfernt.
* Azure.Storage
    - Ein Upgrade auf Azure Storage-Clientbibliothek 8.6.0 und Azure Storage DataMovement-Bibliothek 0.6.5 wurde durchgeführt.

## <a name="20171110-version-501"></a>10.11.2017 – Version 5.0.1
* Problem beim Laden von Assemblys behoben, das dazu führte, dass einige Cmdlets in den folgenden Modulen nicht erfolgreich ausgeführt werden konnten:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>08.11.2017 – Version 5.0.0
* HINWEIS:  Hierbei handelt es sich um eine Version mit grundlegenden Änderungen. Eine vollständige Liste mit den grundlegenden Änderungen finden Sie im Migrationshandbuch (https://aka.ms/azps-migration-guide).
* Alle Cmdlets im AzureRM unterstützen jetzt die Onlinehilfe.
  - Führen Sie „Get-Help“ mit dem Parameter „-Online“ aus, um die Onlinehilfe in Ihrem Standardinternetbrowser zu öffnen.
* AnalysisServices
  * Der Befehl „Synchronize-AzureAsInstance“ wurde korrigiert und kann mit der neuen AsAzure-REST-API für die Synchronisierung verwendet werden.
* ApiManagement
  * Informationen zu grundlegenden Änderungen, die in dieser Version für „ApiManagement“ vorgenommen wurden, finden Sie im Migrationshandbuch.
  * Cmdlet „Get-AzureRmApiManagementUser“ aktualisiert, um folgendes Problem zu beheben: https://github.com/Azure/azure-powershell/issues/4510
  * Cmdlet „New-AzureRmApiManagementApi“ aktualisiert, um die API mit leerem Pfad zu erstellen: https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
  * Befehle zum Abrufen/Erstellen/Entfernen von Application Insights-Ressourcen hinzugefügt
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Befehle zum Abrufen/Aktualisieren von Preisen/Tagesobergrenzen von Application Insights-Ressourcen hinzugefügt
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Befehle zum Abrufen/Erstellen/Aktualisieren/Entfernen des fortlaufenden Exports von Application Insights-Ressourcen hinzugefügt
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Befehle zum Abrufen/Erstellen/Entfernen der API-Schlüssel von Application Insights-Ressourcen hinzugefügt
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * Neue Parameter zu `New-AzureRmBatchAccount` hinzugefügt
    - `PoolAllocationMode`: Der Zuordnungsmodus, der beim Erstellen von Pools im Batch-Konto verwendet werden soll. Wenn Sie ein Batch-Konto erstellen möchten, das Poolknoten im Abonnement des Benutzers zuordnet, legen Sie diesen Modus auf `UserSubscription` fest.
    - `KeyVaultId`: Die Ressourcen-ID des Azure-Schlüsseltresors, der dem Batch-Konto zugeordnet ist.
    - `KeyVaultUrl`: Die URL des Azure-Schlüsseltresors, der dem Batch-Konto zugeordnet ist.
  * Parameter für `New-AzureBatchTask` aktualisiert
    - Der Switch `RunElevated` wurde entfernt. Der Parameter `UserIdentity` wurde hinzugefügt und ersetzt `RunElevated`. Das entsprechende Verhalten kann erreicht werden, indem `PSUserIdentity` wie folgt konstruiert wird:
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - Parameter `AuthenticationTokenSettings` hinzugefügt Mit diesem Parameter können Sie angeben, dass der Batch-Dienst ein Authentifizierungstoken für die Aufgabe bereitstellen soll, wenn sie ausgeführt wird. Dadurch müssen keine Batch-Kontoschlüssel an die Aufgabe übergeben werden, um Anforderungen an den Batch-Dienst auszugeben.
    - Parameter `ContainerSettings` hinzugefügt
      - Mit diesem Parameter können Sie angeben, dass der Batch-Dienst die Aufgabe innerhalb eines Containers ausführen soll.
    - Parameter `OutputFiles` hinzugefügt
      - Mit diesem Parameter können Sie die Aufgabe so konfigurieren, dass sie nach Abschluss der Ausführung Dateien in Azure Storage hochlädt.
  * Parameter für `New-AzureBatchPool` aktualisiert
    - Parameter `UserAccounts` hinzugefügt
      - Dieser Parameter definiert Benutzerkonten, die auf den einzelnen Knoten im Pool erstellt werden.
    - `TargetLowPriorityComputeNodes` hinzugefügt und `TargetDedicated` in `TargetDedicatedComputeNodes` umbenannt.
      - `TargetDedicated`-Alias für den Parameter `TargetDedicatedComputeNodes` erstellt
    - Parameter `NetworkConfiguration` hinzugefügt
      - Mit diesem Parameter können Sie die Netzwerkeinstellungen des Pools konfigurieren.
  * Parameter für `New-AzureBatchCertificate` aktualisiert
    - Der Parameter `Password` ist nun eine Zeichenfolge vom Typ `SecureString`.
  * Parameter für `New-AzureBatchComputeNodeUser` aktualisiert
    - Der Parameter `Password` ist nun eine Zeichenfolge vom Typ `SecureString`.
  * Parameter für `Set-AzureBatchComputeNodeUser` aktualisiert
    - Der Parameter `Password` ist nun eine Zeichenfolge vom Typ `SecureString`.
  * Parameter `Name` für `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` und `Remove-AzureBatchNodeFile` in `Path` umbenannt
    - `Name`-Alias für den Parameter `Path` erstellt
  * Objektänderungen
    - Die vollständige Liste finden Sie im Änderungsprotokoll von Batch.
  * Unterstützung für die Azure Active Directory-basierte Authentifizierung hinzugefügt.
    - Rufen Sie zur Verwendung der Azure Active Directory-Authentifizierung mithilfe des Cmdlets `Get-AzureRmBatchAccount` ein `BatchAccountContext`-Objekt ab, und übergeben Sie `BatchAccountContext` an den Parameter `-BatchContext` eines Batch-Dienst-Cmdlets. Die Azure Active Directory-Authentifizierung ist für Konten mit `PoolAllocationMode = UserSubscription` obligatorisch.
    - Für bereits vorhandene Konten oder neue Konten, die mit `PoolAllocationMode = BatchService` erstellt werden, können Sie weiterhin die Authentifizierung mit gemeinsam verwendetem Schlüssel verwenden, indem Sie mithilfe des Cmdlets `Get-AzureRmBatchAccoutKeys` ein `BatchAccountContext`-Objekt abrufen.
* Compute
  * Befehle der Azure Disk Encryption-Erweiterung
    - Neuer Parameter für „Set-AzureRmVmDiskEncryptionExtension“: „-EncryptFormatAll“ zum Verschlüsseln/Formatieren von Datenträgern
    - Neue Parameter für „Set-AzureRmVmDiskEncryptionExtension“: „-ExtensionPublisherName“ und „-ExtensionType“ zum Wechseln zu anderen Versionen der Erweiterung
    - Neue Parameter für „Disable-AzureRmVmDiskEncryption“: „-ExtensionPublisherName“ und „-ExtensionType“ zum Wechseln zu anderen Versionen der Erweiterung
    - Neue Parameter für „Get-AzureRmVmDiskEncryptionStatus“: „-ExtensionPublisherName“ und „-ExtensionType“ zum Wechseln zu anderen Versionen der Erweiterung
* DataLakeAnalytics
  * Informationen zu grundlegenden Änderungen, die in dieser Version für „DataLakeAnalytics“ vorgenommen wurden, finden Sie im Migrationshandbuch.
  * Einer der beiden Ausgabetypen von „Get-AzureRmDataLakeAnalyticsAccount“ wurde geändert.
    - „List\<DataLakeAnalyticsAccount>“ in „List\<PSDataLakeAnalyticsAccountBasic>“
    - Bei den Eigenschaften von „PSDataLakeAnalyticsAccountBasic“ handelt es sich um eine echte Teilmenge der Eigenschaften von „DataLakeAnalyticsAccount“.
    - Die zusätzlichen Eigenschaften in „DataLakeAnalyticsAccount“ werden von dem Dienst nicht zurückgegeben.  Diese Änderung dient dazu, dies korrekt wiederzugeben. Die zusätzlichen Eigenschaften sind zwar weiterhin in „PSDataLakeAnalyticsAccountBasic“ enthalten, werden aber als veraltet gekennzeichnet.
  * Einer der beiden Ausgabetypen von „Get-AzureRmDataLakeAnalyticsJob“ wurde geändert.
    - „List\<JobInformation>“ in „List\<PSJobInformationBasic>“
    - Bei den Eigenschaften von „PSJobInformationBasic“ handelt es sich um eine echte Teilmenge der Eigenschaften von „JobInformation“.
    - Die zusätzlichen Eigenschaften in „JobInformation“ werden von dem Dienst nicht zurückgegeben.  Diese Änderung dient dazu, dies korrekt wiederzugeben. Die zusätzlichen Eigenschaften sind zwar weiterhin in „PSJobInformationBasic“ enthalten, werden aber als veraltet gekennzeichnet.
* DataLakeStore
  * Informationen zu grundlegenden Änderungen, die in dieser Version für „DataLakeStore“ vorgenommen wurden, finden Sie im Migrationshandbuch.
  * Einer der beiden Ausgabetypen von „Get-AzureRmDataLakeStoreAccount“ wurde geändert.
    - „List\<PSDataLakeStoreAccount>“ in „List\<PSDataLakeStoreAccountBasic>“
    - Bei den Eigenschaften von „PSDataLakeStoreAccountBasic“ handelt es sich um eine echte Teilmenge der Eigenschaften von „PSDataLakeStoreAccount“.
    - Die zusätzlichen Eigenschaften in „PSDataLakeStoreAccount“ werden von dem Dienst nicht zurückgegeben.  Diese Änderung dient dazu, dies korrekt wiederzugeben. Die zusätzlichen Eigenschaften sind zwar weiterhin in „PSDataLakeStoreAccountBasic“ enthalten, werden aber als veraltet gekennzeichnet.
* Dns
  * Unterstützung für CAA-Eintragstypen in Azure DNS
    - Unterstützt alle Vorgänge für CAA-Eintragstypen
* EventHub
  * Informationen zu grundlegenden Änderungen, die in dieser Version für „EventHub“ vorgenommen wurden, finden Sie im Migrationshandbuch.
* Einblicke
  * Informationen zu grundlegenden Änderungen, die in dieser Version für „Insights“ vorgenommen wurden, finden Sie im Migrationshandbuch.
* Netzwerk
  * Informationen zu grundlegenden Änderungen, die in dieser Version für die Netzwerkkomponente vorgenommen wurden, finden Sie im Migrationshandbuch.
  * Cmdlet hinzugefügt, mit dem verfügbare Internetdienstanbieter für eine bestimmte Azure-Region aufgeführt werden können
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Cmdlet hinzugefügt, mit dem der relative Wartezeitwert für Internetdienstanbieter zwischen einem bestimmten Standort und Azure-Regionen abgerufen werden kann
    - Get-AzureRmNetworkWatcherReachabilityReport
* Profil
  - Set-AzureRmDefault
    - Verwenden Sie dieses Cmdlet, um eine Standardressourcengruppe festzulegen.  Dadurch wird der Parameter „-ResourceGroup“ für einige Cmdlets optional, und es wird der Standardwert verwendet, wenn keine Ressourcengruppe angegeben ist.
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Wenn die angegebene Ressourcengruppe im Abonnement vorhanden ist, wird sie als Standard festgelegt.  Andernfalls wird die Ressourcengruppe erstellt und als Standard festgelegt.
  - Get-AzureRmDefault
    - Verwenden Sie dieses Cmdlet, um die aktuelle Standardressourcengruppe (und später auch andere Standardwerte) abzurufen.
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Verwenden Sie dieses Cmdlet, um die aktuelle Standardressourcengruppe zu entfernen.
    - ```Clear-AzureRmDefault -ResourceGroup```
  - „Add-AzureRmEnvironment“ und „Set-AzureRmEnvironment“
    - Fügen Sie den Parameter „BatchAudience“ hinzu, um die Active Directory-Zielgruppe für Azure Batch anzugeben, die beim Abrufen von Authentifizierungstoken für den Batch-Dienst verwendet werden soll.
* RecoveryServices.Backup
  * Cmdlets für die sofortige Dateiwiederherstellung hinzugefügt
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * SDK-Version für „RecoveryServices.Backup“ auf die neueste Version aktualisiert
  * Tests für die Workload virtueller Azure-Computer aktualisiert, sodass alle für Testläufe erforderlichen Einrichtungsschritte automatisch durchgeführt werden
  * Fehler behoben: https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
  * Änderungen für ASR VMware zu Azure Site Recovery (Cmdlets unterstützen derzeit Vorgänge für Unternehmen zu Unternehmen, Unternehmen zu Azure und Hyper-V zu Azure)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * Unterstützung für AAD-basierten Tresor hinzugefügt
  * Cmdlets zum Verwalten von VCenter-Ressourcen hinzugefügt
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Weitere Cmdlets hinzugefügt
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - Informationen zu grundlegenden Änderungen, die in dieser Version für „ServiceBus“ vorgenommen wurden, finden Sie im Migrationshandbuch.
* Sql
  * Unterstützung für das Auflisten und Abbrechen des asynchronen updateslo-Vorgangs für die Datenbank hinzugefügt
    - Vorhandenes Cmdlet „Get-AzureRmSqlDatabaseActivity“ aktualisiert, um den updateslo-Vorgangsstatus der Datenbank zurückgegeben
    - Neues Cmdlet „Stop-AzureRmSqlDatabaseActivity“ zum Abbrechen des asynchronen updateslo-Vorgangs für die Datenbank hinzugefügt
  * Unterstützung für Zonenredundanz für Datenbanken und Pools für elastische Datenbanken hinzugefügt
    - Switch-Parameter „ZoneRedundant“ zu „New-AzureRmSqlDatabase“ hinzugefügt
    - Switch-Parameter „ZoneRedundant“ zu „Set-AzureRmSqlDatabase“ hinzugefügt
    - Switch-Parameter „ZoneRedundant“ zu „New-AzureRmSqlElasticPool“ hinzugefügt
    - Switch-Parameter „ZoneRedundant“ zu „Set-AzureRmSqlElasticPool“ hinzugefügt
  * Unterstützung für Server-DNS-Aliase hinzugefügt
    - Cmdlet „Get-AzureRmSqlServerDnsAlias“ hinzugefügt, um Server-DNS-Aliase nach Server und Aliasname oder eine Liste mit Server-DNS-Aliasen für eine Azure SQL Server-Instanz abzurufen
    - Cmdlet „New-AzureRmSqlServerDnsAlias“ zum Erstellen eines neuen Server-DNS-Alias für eine bestimmte Azure SQL Server-Instanz hinzugefügt
    - Cmdlet „Set-AzurermSqlServerDnsAlias“ hinzugefügt, um die Aktualisierung einer Azure SQL Server-Instanz zu ermöglichen, auf die der Server-DNS-Alias verweist
    - Cmdlet „Remove-AzureRmSqlServerDnsAlias“ zum Entfernen eines Server-DNS-Alias für eine Azure SQL Server-Instanz hinzugefügt
* Azure.Storage
  * Upgrade auf Azure Storage-Clientbibliothek 8.5.0 und Azure Storage DataMovement-Bibliothek 0.6.3 durchgeführt
  * Supportfeature für Dateifreigabemomentaufnahmen hinzugefügt
    - Parameter „SnapshotTime“ zu „Get-AzureStorageShare“ hinzugefügt
    - Parameter „IncludeAllSnapshot“ zu „Remove-AzureStorageShare“ hinzugefügt
