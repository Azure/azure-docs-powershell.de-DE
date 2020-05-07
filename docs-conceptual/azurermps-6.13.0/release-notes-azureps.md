---
title: Azure PowerShell-Änderungsprotokoll | Microsoft-Dokumentation
description: Hierbei handelt es sich um einen Verlauf der Änderungen, die in der neuesten Version an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eecd66ddf433cc2543ceeaef1519d69179f2f099
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534456"
---
# <a name="release-notes"></a>Versionshinweise

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Hierbei handelt es sich um eine Liste der Änderungen, die in dieser Version an Azure PowerShell vorgenommen wurden.

---
## <a name="6130---november-2018"></a>6.13.0: November 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

#### <a name="azurermautomation"></a>AzureRM.Automation
* Swagger-basierte Azure Automation-Cmdlets
* Cmdlets zur Updateverwaltung hinzugefügt
* Cmdlets zur Quellcodeverwaltung hinzugefügt
* Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt
* DSC-Befehl für die Knotenregistrierung korrigiert

#### <a name="azurermcompute"></a>AzureRM.Compute
* Identitätsproblem für SystemAssigned-Identität korrigiert
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert

#### <a name="azurermnetwork"></a>AzureRM.Network
* Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError
* ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt
* Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt 
* Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben
* Richtlinienzeitzone in Großschreibung geändert

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

#### <a name="azurermrelay"></a>AzureRM.Relay
* Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht

#### <a name="azurermresources"></a>AzureRM.Resources
* Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert
* Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt
* Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt

#### <a name="azurermsql"></a>AzureRM.Sql
* Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert
    - Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen
    - Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.
    - Set-AzureRmSqlServerAuditing
    - Get-AzureRmSqlServerAuditing
    - Set-AzureRmSqlDatabaseAuditing
    - Get-AzureRmSqlDatabaseAuditing
* Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben

## <a name="6120---november-2018"></a>6.12.0: November 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird
* Parameter „TenantId“ im Cmdlet „Connect-AzureRmAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt
* Beschreibung von „TenantId“ für „Connect-AzureRmAccount“ aktualisiert
* Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert
    - https://github.com/Azure/azure-powershell/issues/6936
* Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben
    - https://github.com/Azure/azure-powershell/issues/7453
* Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben
    - https://github.com/Azure/azure-powershell/issues/7462
* Problem behoben, das zur Auslösung von „Disconnect-AzureRmAccount“ führte, wenn keine Verbindung bestand
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* DLL-Dateiname des Cmdlets in „Microsoft.Azure.Commands.Automation.dll“ umbenannt

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Vorgang „Get-AzureRmCognitiveServicesAccountSkus“ hinzugefügt

#### <a name="azurermcompute"></a>AzureRM.Compute
* Cmdlets „Add-AzureRmVmssVMDataDisk“ und „Remove-AzureRmVmssVMDataDisk“ hinzugefügt
* „Get-AzureRmVMImage“ zeigt „AutomaticOSUpgradeProperties“ an.
* Problem behoben, aufgrund dessen die Optionswerte „SetAzureRmVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Aktualisierung des DataLake-Pakets auf 1.1.10
* Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt

#### <a name="azurerminsights"></a>AzureRM.Insights
* Problem Nr. 7267 behoben (Bereich für automatische Skalierung)
    - Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)
* Problem Nr. 7513 behoben [Insights] „Set-AzureRMDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.
    - Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.

#### <a name="azurermnetwork"></a>AzureRM.Network
* „PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Cmdlets für Richtlinienwartung hinzugefügt

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Unterstützung für Azure-Dateifreigaben in Wiederherstellungsdiensten hinzugefügt

#### <a name="azurermresources"></a>AzureRM.Resources
* Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402
    - Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzureRmResource“

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Hinzufügen des Zertifikats zu Linux VMSS korrigiert
* „Add-AzureRmServiceFabricClusterCertificate“ korrigiert
    - Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)
    - Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)
* „Update-AzureRmServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird

## <a name="6110---october-2018"></a>6.11.0 – Oktober 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Problem mit „Get-AzureRmSubscription“ in CloudShell behoben
* Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird

#### <a name="azurermbackup"></a>AzureRM.Backup
* Azure Backup-Cmdlets als veraltet markiert.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzureRmVm“ der beschleunigte Netzwerkbetrieb aktiviert wird
* ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Unterstützung für VNET-Regeln hinzugefügt
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: Ruft die VNET-Regel für Azure Data Lake Store ab oder listet sie auf.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine VNET-Regel hinzu.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: Ändert die angegebene VNET-Regel im angegebenen Data Lake Store-Konto.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: Löscht eine VNET-Regel für Azure Data Lake Store.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.
* ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.

#### <a name="azurermresources"></a>AzureRM.Resources
* Problem behoben, aufgrund dessen „Get-AzureRMRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist) indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde. Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.

## <a name="6100---october-2018"></a>6.10.0 – Oktober 2018
#### <a name="azurestorage"></a>Azure.Storage
* Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* „Get-AzureRmCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Korrektur von „Get-AzureRmVM -ResourceGroupName <rg>“ sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden
* Der Cmdlet-Hilfe zu „New-AzureRmVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.
* Tippfehler in der Azure Disk Encryption-Statusmeldung behoben

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.

#### <a name="azurermnetwork"></a>AzureRM.Network
* NetworkProfile-Funktionalität wurde hinzugefügt. Neue Cmdlets hinzugefügt
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Dienstzuordnungslink in Subnetzmodell hinzugefügt
* Cmdlets „New-AzureRmVirtualNetworkTap“, „Get-AzureRmVirtualNetworkTap“, „Set-AzureRmVirtualNetworkTap“, „Remove-AzureRmVirtualNetworkTap“ hinzugefügt
* Cmdlets „Set-AzureRmNEtworkInterfaceTapConfig“, „Get-AzureRmNEtworkInterfaceTapConfig“, „Remove-AzureRmNEtworkInterfaceTapConfig“ hinzugefügt

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig. P5 in Popup „PSArgumentCompleter“ hinzugefügt

#### <a name="azurermresources"></a>AzureRM.Resources
* Fehlender Parameter „-Mode“ zu „Set-AzureRmPolicyDefinition“ hinzugefügt
* Cmdlet-Fehler bei „Fix Get-AzureRmProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält

#### <a name="azurermsql"></a>AzureRM.Sql
* Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben

#### <a name="azurermstorage"></a>AzureRM.Storage
* Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Neues Cmdlet „Get-AzureRMWebAppContainerContinuousDeploymentUrl“ zum Abruf der Webhook-URL von Continuous Deployment für Container
* Neue Cmdlets „New-AzureRMWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App

## <a name="690---september-2018"></a>6.9.0 – September 2018
#### <a name="general"></a>Allgemein
* AzureRM.SignalR wurde dem Rollupmodul AzureRM hinzugefügt

#### <a name="azurermprofile"></a>AzureRM.Profile
* Kleinere Änderungen am allgemeinen Speichercode
* Hilfedateien aktualisiert, um vollständige Parametertypen einzubinden.
* „-ServicePrincipal“ im Parametersatz „ServicePrincipalCertificateWithSubscriptionId“ in nicht obligatorisch geändert 

#### <a name="azurestorage"></a>Azure.Storage
* Unterstützung für die Erstellung des Speicherkontexts mit OAuth. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Standard_Microsoft in SKU für CDN-Preise hinzugefügt. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* Abhängigkeiten für Key Vault und Storage in allgemeine Abhängigkeiten verschieben
* Unterstützung für weitere VM-Größen zu AEM-Cmdlets hinzufügen
* Parameter „PublicIPPrefix“ zu „New-AzureRmVmssIpConfig“ hinzufügen
* Parameter „ResourceId“ zu Cmdlet „Invoke-AzureRmVMRunCommand“ hinzufügen
* Cmdlet „Invoke-AzureRmVmssVMRunCommand“ hinzufügen

#### <a name="azurermdns"></a>AzureRM.Dns
* Unterstützung für Aliaseintrag während der Erstellung des DNS-Eintrags hinzugefügt

#### <a name="azurerminsights"></a>AzureRM.Insights
* Probleme #6833 und #7102 behoben (Bereich „Diagnoseeinstellungen“)
    - Probleme mit dem Standardnamen, also „service“, beim Erstellen und Auflisten/Abrufen von Diagnoseeinstellungen
    - Probleme beim Erstellen von Diagnoseeinstellungen mit Kategorien
* Meldung zur Einstellung der Unterstützung für Metrikaggregationsintervall-Parameter
    - Aggregationsintervall-Parameter werden weiterhin akzeptiert (Änderung ohne Funktionsbeeinträchtigung), aber sie werden auf dem Back-End ignoriert, da nur PT1M gültig ist

#### <a name="azurermnetwork"></a>AzureRM.Network
* Änderungen an LoadBalancer-Cmdlets
  - LoadBalancerInboundNatPoolConfig: Parameter IdleTimeoutInMinutes, EnableFloatingIp und EnableTcpReset hinzugefügt
  - LoadBalancerInboundNatRuleConfig: Parameter EnableTcpReset hinzugefügt
  - LoadBalancerRuleConfig: Parameter EnableTcpReset hinzugefügt
  - LoadBalancerProbeConfig: Unterstützung für Wert „Https“ für Parameter „Protocol“ hinzugefügt
* Neue Befehle für neue Unterressource „OutboundRule“ von LoadBalancer hinzugefügt
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Neue HostedWorkloads-Eigenschaft für PSNetworkInterface hinzugefügt
* Neue Cmdlets für Feature: Azure Firewall über ARM
  - Get-AzureRmFirewall hinzugefügt
  - Set-AzureRmFirewall hinzugefügt
  - New-AzureRmFirewall hinzugefügt
  - Remove-AzureRmFirewall hinzugefügt
  - New-AzureRmFirewallApplicationRuleCollection hinzugefügt
  - New-AzureRmFirewallApplicationRule hinzugefügt
  - New-AzureRmFirewallNatRuleCollection hinzugefügt
  - New-AzureRmFirewallNatRule hinzugefügt
  - New-AzureRmFirewallNetworkRuleCollection hinzugefügt
  - New-AzureRmFirewallNetworkRule hinzugefügt
* Unterstützung für vertrauenswürdiges Stammzertifikat und Konfiguration der automatischen Skalierung in Application Gateway hinzugefügt
  - Neue Cmdlets hinzugefügt:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Cmdlets mit optionalem Parameter „-TrustedRootCertificate“ aktualisiert
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Cmdlets mit optionalem Parameter „-AutoscaleConfiguration“ aktualisiert
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Cmdlet für Schnittstellenendpunkt Get-AzureInterfaceEndpoint hinzugefügt
* Unterstützung für mehrere Adresspräfixe in einem Subnetz hinzugefügt. Aktualisierte Cmdlets:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Cmdlets für die Subnetzdelegierung hinzufügen.
  - New-AzureRmDelegation: Erstellt eine neue Delegierung, die einem Subnetz hinzugefügt werden kann
  - Remove-AzureRmDelegation: Nutzt ein Subnetz und entfernt den bereitgestellten Delegierungsnamen aus diesem Subnetz
  - Add-AzureRmDelegation: Nutzt ein Subnetz und fügt den angegebenen Dienstnamen diesem Subnetz als Delegierung hinzu
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Unterstützung für verwalteten Datenträger

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Insights-Abhängigkeit aktualisiert.

#### <a name="azurermresources"></a>AzureRM.Resources
* New-AzureRmResourceGroupDeployment mit neuem Parameter „RollbackAction“ aktualisieren
    - Unterstützung für OnErrorDeployment mit dem neuen Parameter hinzufügen.
* Unterstützung für verwaltete Identität in Richtlinienzuweisungen.
* Parameter mit Standardwerten sind nicht mehr erforderlich, wenn eine Richtlinie mit „New-AzureRmPolicyAssignment“ zugewiesen wird
* Neues Cmdlet „Get-AzureRmPolicyAlias“ zum Abrufen von Richtlinienaliasen hinzufügen

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Problem #7161 behoben

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* SKU-Namen auf Free_F1 und Standard_S1 aktualisieren
* Versionsfeld zum PSSignalRResource-Objekt und Verbindungszeichenfolge zum PSSignalRKeys-Objekt hinzufügen.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Unterstützung für Unveränderlichkeitsrichtlinie in AzureRm.Storage 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Zwei neue Cmdlets hinzugefügt: Get-AzureRmDeletedWebApp und Restore-AzureRmDeletedWebApp
* New-AzureRmAppServicePlan -HyperV-Switch für „App Service-Plan erstellen“ mit Windows-Container hinzugefügt
* New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Neue Parameter (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) für die Erstellung und Verwaltung der Windows-Container-App hinzugefügt

## <a name="681---august-2018"></a>6.8.1: August 2018
#### <a name="general"></a>Allgemein
* Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.
* Allgemeine Laufzeitassemblys aktualisiert

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.
* Problem https://github.com/Azure/azure-powershell/issues/6603 behoben
    - Die Cmdlets „Import-AzureRmApiManagementApi“ und „*-AzureRmApiManagementCertificate“ können jetzt relative Pfade verarbeiten.
* Problem https://github.com/Azure/azure-powershell/issues/6879 behoben
    - „CertificateInformation“ ist eine festlegbare Eigenschaft, die die ordnungsgemäße Funktionsweise des Cmdlets „Set-AzureRmApiManagement“ ermöglicht. Behoben durch Upgrade auf NuGet-Paket „4.0.4-preview“
* Problem https://github.com/Azure/azure-powershell/issues/6853 behoben
    - OData-Filter für die Suche anhand des Namens korrigiert (Produkt)
* Problem https://github.com/Azure/azure-powershell/issues/6814 behoben
    - OData-Filter für die Suche anhand des Namens korrigiert (API)
* Unterstützung für AzureMonitor-Protokollierung hinzugefügt


#### <a name="azurermcompute"></a>AzureRM.Compute
* Problem des fehlenden Ziels in der Fehlerausgabe behoben
* Problem mit dem Speicherkontotyp für den virtuellen Computer mit verwaltetem Datenträgern behoben
* Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.
* AEM-Erweiterungs-Cmdlets für andere Umgebungen (etwa Azure China) korrigiert

#### <a name="azurermnetwork"></a>AzureRM.Network
* Standarddarstellung der Cmdlet-Ausgabe in Tabellenansicht geändert

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Fehler in „Update-AzureRmPowerBIEmbeddedCapacity“ beim Skalieren der angehaltenen Kapazität behoben


#### <a name="azurermresources"></a>AzureRM.Resources
* Problem beim Erstellen verwalteter Anwendungen über Marketplace behoben

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Behobene Probleme
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Unterstützung für Routingmethode „MultiValue“ hinzugefügt
    - Neuer Parameter „MaxReturn“ für Routingtyp „MultiValue“
* Unterstützung für Subnetzroutingmethode hinzugefügt
    - Unterstützung für IP-Adressbereiche (Subnetze) in Endpunkten
* Unterstützung für benutzerdefinierte Header in Profilen hinzugefügt
* Unterstützung für erwartete Statuscodebereiche in Profilen hinzugefügt
* Unterstützung für benutzerdefinierte Header in Endpunkten hinzugefügt

## <a name="680---august-2018"></a>6.8.0: August 2018
#### <a name="general"></a>Allgemein
* Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Ablaufeigenschaft zu Token hinzugefügt, die während „Connect-AzureRmAccount“ zurückgegeben werden

#### <a name="azurermcompute"></a>AzureRM.Compute
* Problem des fehlenden Ziels in der Fehlerausgabe behoben
* Problem mit dem Speicherkontotyp für den virtuellen Computer mit verwaltetem Datenträgern behoben
* AEM-Erweiterungs-Cmdlets für andere Umgebungen (etwa Azure China) korrigiert

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Beispiele für „New-AzureRmIotHubExportDevices“ und „New-AzureRmIotHubImportDevices“ korrigiert

#### <a name="azurermnetwork"></a>AzureRM.Network
* Standarddarstellung von Modellen in Tabellenansicht geändert

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Fehler in „Update-AzureRmPowerBIEmbeddedCapacity“ beim Skalieren der angehaltenen Kapazität behoben

#### <a name="azurermresources"></a>AzureRM.Resources
* Problem beim Erstellen der verwalteten Anwendung über Marketplace behoben

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Fehlerbehebung
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Unterstützung für Routingmethode „MultiValue“
    - Neuer Parameter „MaxReturn“ für Routingtyp „MultiValue“
* Unterstützung für Subnetzroutingmethode
    - Unterstützung für IP-Adressbereiche (Subnetze) in Endpunkten
* Unterstützung für benutzerdefinierte Header in Profilen
* Unterstützung für erwartete Statuscodebereiche in Profilen
* Unterstützung für benutzerdefinierte Header in Endpunkten

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Das Problem, dass die Standardressourcengruppe falsch festgelegt wurde, wurde behoben.

## <a name="670---august-2018"></a>6.7.0: August 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert
* Benutzer-ID zum Standardkontextnamen hinzugefügt, um Kontextkonflikte zu vermeiden
    - https://github.com/Azure/azure-powershell/issues/6489
* Probleme mit „Clear-AzureRmContext“ behoben, die Fehler beim Auswählen eines Kontexts verursacht haben (6398)
* Ermöglicht, dass für „Connect-AzureRmAccount“ die Mandantendomäne an den Parameter „-TenantId“ übergeben wird
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Begrenzung von 5 TB für das Kontingent der Azure-Dateifreigabe entfernt
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermautomation"></a>AzureRM.Automation
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermbackup"></a>AzureRM.Backup
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermbatch"></a>AzureRM.Batch
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermbilling"></a>AzureRM.Billing
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermcompute"></a>AzureRM.Compute
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert
* EvictionPolicy-Parameter zu „New-AzureRmVmssConfig“ hinzugefügt
* Standort in „DiskFileParameterSet“ von „New-AzureRmVm“ angeben, wenn kein Ort angegeben ist
* Parameterbeschreibung in „Save-AzureRmVMImage“ korrigiert
* Cmdlet „Get-AzureRmVMDiskEncryptionStatus“ für bestimmte Szenarien im Zusammenhang mit einem Durchlauf korrigiert

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Debuggen korrigiert, wenn „DebugPreference“ über die PowerShell-Befehlszeile festgelegt wird
* Beispiel für „Set-AzureRmDataLakeStoreItemAcl“ aktualisiert
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert
* Beispiel für „Set-AzureRmDataLakeStoreItemAclEntry“ aktualisiert

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermdns"></a>AzureRM.Dns
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurerminsights"></a>AzureRM.Insights
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermmedia"></a>AzureRM.Media
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermnetwork"></a>AzureRM.Network
* Beispiel für „Set-AzureRmLocalNetworkGateway“ hinzugefügt
* Beispiele und Beschreibungen für „Add-AzureRmVirtualNetworkGatewayIpConfig“, „Get-AzureRmVirtualNetworkGatewayConnectionSharedKey“ und „New-AzureRmVirtualNetworkGatewayConnection“ hinzugefügt
* Beispiele für „Remove-AzureRmVirtualNetworkGatewayIpConfig“ und „Reset-AzureRmVirtualNetworkGateway“ hinzugefügt
* Beispiel für „Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey“ hinzugefügt
* Beispiel für „Set-AzureRmVirtualNetworkGatewayConnectionSharedKey“ hinzugefügt
* Beispiel für „Set-AzureRmVirtualNetworkGatewayConnection“ hinzugefügt
* Cmdlets für „ApplicationSecurityGroup“, „RouteTable“ und „Usage“ mithilfe des aktuellen Code-Generators erneut erstellt
* Deutlichere Formulierung der Fehlermeldung für „Get-AzureRmVirtualNetworkSubnetConfig“, wenn ein nicht vorhandenes Subnetz abgerufen wird

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Richtlinienfilter zum Cmdlet „Get-AzureRmRecoveryServicesBackItem“ hinzugefügt. Der Befehl gibt die Liste der Sicherungselemente zurück, die durch die angegebene Richtlinien-ID geschützt sind.
* „Microsoft.Azure.Management.RecoveryServices.Backup“ auf Version 3.0.0-preview aktualisiert
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert
* TargetResourceGroupName-Parameter zu „Restore-AzureRmRecoveryServicesBackupItem“ hinzugefügt. Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden. Gilt für die Sicherung des virtuellen Computers mit verwalteten Datenträgern.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermrelay"></a>AzureRM.Relay
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermresources"></a>AzureRM.Resources
* Unterstützung der Vorlagenbereitstellung im Abonnementbereich. Neue Cmdlets hinzugefügt:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Problem behoben, aufgrund dessen beim Übergeben eines Kontexts an „Set-AzureRmResource“ ein Fehler auftrat
    - https://github.com/Azure/azure-powershell/issues/5705
* Beispiel in „New-AzureRmResourceGroupDeployment“ korrigiert
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermsql"></a>AzureRM.Sql
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermstorage"></a>AzureRM.Storage
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermtags"></a>AzureRM.Tags
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Auf die aktuelle Version von Azure ClientRuntime aktualisiert

## <a name="660---july-2018"></a>6.6.0 – Juli 2018
#### <a name="general"></a>Allgemein
* Alle Hilfedateien aktualisiert, um vollständige Parametertypen und die richtigen Eingabe/Ausgabe-Typen einzuschließen.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Bibliothek „Common.Strategy“ aktualisiert, um überprüfen zu können, ob die aktuelle Konfiguration für eine Ressource mit der Zielressource kompatibel ist.
* ps1xml-Typen zu „Common.Storage“ hinzugefügt

#### <a name="azurestorage"></a>Azure.Storage
* Unterstützung zum Abrufen von Speicherkontext aus „DefaultProfile“ hinzugefügt
* „Ps1XmlAttribute“ zu Typeneigenschaften von Cmdlet-Ausgaben hinzugefügt

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Problem https://github.com/Azure/azure-powershell/issues/6370 behoben
    - Fehler in Automapper behoben, um „PsApiManagementApi“ in „ApiContract“ zu verschieben
* Problem https://github.com/Azure/azure-powershell/issues/6515 behoben
    - Fehler in „File.Save“ behoben, um Überladung mit Codierungstyp zu vermeiden
* Problem https://github.com/Azure/azure-powershell/issues/6560 behoben
    - Upgrade auf Nuget-Version 4.0.3 durchgeführt, in der Musterausnahme in „apiId“ behoben wurde

#### <a name="azurermcompute"></a>AzureRM.Compute
* Das Problem, aufgrund dessen beim Erstellen eines virtuellen Computers mithilfe von „DiskFileParameterSet“ in „New-AzureRmVm“ wegen einer Umbenennung des Speicherkontotyps „PremiumLRS“ ein Fehler auftrat, wurde behoben.
* Cmdlet „Invoke-AzureRmVMRunCommand“ korrigiert
* „Get-AzureRmAvailabilitySet“ aktualisiert, um die Auflistung aller Verfügbarkeitsgruppen in einem Abonnement zu ermöglichen.  (ResouceGroupName-Parameter ist jetzt optional.)
* „SimpleParameterSet“ von „New-AzureRmVm“ aktualisiert, um Accelerated Networking auf kompatiblen virtuellen Computern zu ermöglichen.
* Einfacher Parametersatz „New-AzureRmVmss“ aktualisiert, sodass das Erstellen der VMSS fehlschlägt, wenn bereits ein benutzerdefinierter LB vorhanden ist.
* Beispiel für „New-AzureRmDisk“ aktualisiert
* Beispiel für „New-AzureRmVM“ hinzugefügt
* Beschreibung für „Set-AzureRmVMOSDisk“ aktualisiert
* Beispiel 1 für „Set-AzureRmVMBginfoExtension“ aktualisiert, um Rechtschreibung und Präfix zu korrigieren. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK-Version auf 1.1.0 aktualisiert.
* Unterstützung der Freigabe der selbstgehosteten Integration Runtime über Data Factorys hinweg.
     - Neuer Parameter „-SharedIntegrationRuntimeResourceId“ zu Cmdlet „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt.
     - Neuer optionaler Parameter „-LinkedDataFactoryName“ zu Cmdlet „Remove-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DataPlane SDK-Version (Microsoft.Azure.DataLake.Store) auf 1.1.9 aktualisiert

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Piping für „InputObject“ und „ResourceId“ in Entfernungs-Cmdlets aktualisiert

#### <a name="azurerminsights"></a>AzureRM.Insights
* Formatierung von „OutputType“ in Hilfedateien korrigiert
* Verwendung von Microsoft.Azure.Management.Monitor SDK 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Piping-Problem in „Set-AzureRmKeyVaultAccessPolicy“ behoben

#### <a name="azurermnetwork"></a>AzureRM.Network
* Beispiele für LoadBalancerInboundNatPoolConfig-Cmdlets hinzugefügt.

#### <a name="azurermresources"></a>AzureRM.Resources
* Problem beim Angeben sowohl des Tag-Namens als auch des Werts für „Get-AzureRmResource“ behoben
    - https://github.com/Azure/azure-powershell/issues/6765
* Piping-Szenario mit „Set-AzureRmResource“ korrigiert

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Piping für „InputObject“ und „ResourceId“ in Entfernungs-Cmdlets aktualisiert
* Einige Probleme behoben
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Unterstützung für Advanced Threat Protection für Server bei folgenden Cmdlets hinzugefügt:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Unterstützung für Sicherheitsrisikobewertung bei folgenden Cmdlets hinzugefügt:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Beispiel in „Remove-AzureRmSqlServerFirewallRule“ korrigiert
* Falsche Verarbeitung von „datetime“ für nicht US-basierte Kultur in „Get-AzureSqlSyncGroupLog“ korrigiert

#### <a name="azurermstorage"></a>AzureRM.Storage
* „Ps1XmlAttribute“ zu Typeneigenschaften von Cmdlet-Ausgaben hinzugefügt
* Cmdlet-Ausgabe von „StorageAccount“ in Tabellenansicht anzeigen
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Falsche Anweisung aus Tag-Cmdlet-Hilfe entfernt
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 – Juli 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Hilfe für „Get-AzureRmContextAutosaveSetting“ aktualisiert

#### <a name="azurestorage"></a>Azure.Storage
* Unterstützung des Blob- oder Dateiuploads mit lesegeschütztem SAS-Token
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Erforderliche Eigenschaft „ResourceGroupName“ zu AS hinzugefügt.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Hilfe aktualisiert und Beispiel für „New-AzureRMAutomationSchedule“ hinzugefügt

#### <a name="azurermcompute"></a>AzureRM.Compute
* Parameter „-Tag“ zu „Update/New-AzureRmAvailabilitySet“ hinzugefügt
* Beispiel für „Add-AzureRmVmssExtension“ hinzugefügt
* Beispiele für „Remove-AzureRmVmssExtension“ hinzugefügt
* Hilfe für „Set-AzureRmVMAccessExtension“ aktualisiert
* „SimpleParameterSet“ für „New-AzureRmVmss“ so aktualisiert, dass „SinglePlacementGroup“ standardmäßig auf „false“ festgelegt ist, und Switch-Parameter „SinglePlacementGroup“ hinzugefügt, der dem Benutzer das Erstellen der VMSS in einer einzelnen Platzierungsgruppe ermöglicht.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Schreibgeschützte Eigenschaft „PendingReplicationOperationsCount“ zur Klasse „PSEventHubDRConfigurationAttributes“ hinzugefügt, welche die Anzahl der ausstehenden Replikationsvorgänge während der Replikation angibt

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Fehlermeldung für „Set-AzureRmKeyVaultAccessPolicy“ aktualisiert

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Fehler „Parametersatz konnte nicht aufgelöst werden“ in „New-AzureRmLogicApp“behoben

#### <a name="azurermnetwork"></a>AzureRM.Network
* Peering über mehrere virtuelle Netzwerke in mehreren Mandanten für „Set/Add-AzureRmVirtualNetworkPeering“ aktiviert
* Folgende Cmdlets für Application Gateway aktualisiert
    - New-AzureRmApplicationGateway: EnableFIPS-Flag und Zonenunterstützung hinzugefügt
    - New-AzureRmApplicationGatewaySku: Neue SKUs „Standard_v2“ und „WAF_v2“ hinzugefügt
    - Set-AzureRmApplicationGatewaySku: Neue SKUs „Standard_v2“ und „WAF_v2“ hinzugefügt
* RouteTable-Cmdlets mit aktueller Generatorversion erneut generiert

#### <a name="azurermrelay"></a>AzureRM.Relay
* Markdowndateien aktualisiert, Problem mit Parametername in Beispiel behoben

#### <a name="azurermresources"></a>AzureRM.Resources
* Roleassignment- und roledefinition-Cmdlets aktualisiert:
    - Zusätzliche roledefinition-Aufrufe entfernt, die als Teil des Pagings durchgeführt wurden.
* Get-AzureRmRoleAssignment-Cmdlet korrigiert
    - Befehlsparameterfunktion von „-ExpandPrincipalGroups“ korrigiert
* Problem mit „Get-AzureRmResource“ behoben, aufgrund dessen die Groß-/Kleinschreibung des Parameters „-ResourceType“ beachtet wurde

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* top- und skip-Parameter zu Listen-Cmdlets hinzugefügt
* Cmdlets für die Migration von Standard- zu Premium-Namespace hinzugefügt:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* Schreibgeschützte Eigenschaft „PendingReplicationOperationsCount“ zur Klasse „PSServiceBusDRConfigurationAttributes“ hinzugefügt, welche die Anzahl der ausstehenden Replikationsvorgänge während der Replikation angibt

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Beispiel für „New-AzureRmServiceFabricCluster“ hinzugefügt

#### <a name="azurermsql"></a>AzureRM.Sql
* Neue Cmdlets für „Management.Sql“ hinzugefügt, um Kunden das Hinzufügen des TDE-Zertifikats zu einer SQL Server-Instanz oder einer verwalteten Instanz zu ermöglichen
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Wenn `Set-AzureRmWebApp -AssignIdentity` und `Set-AzureRmWebAppSlot -AssignIdentity` auf „false“ festgelegt sind, wird jetzt die Identity-Eigenschaft aus dem Websiteobjekt entfernt. Auch das Vorschau-Tag wird entfernt.
* `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`-Beispiel aktualisiert
* Unterstützung von `Set-AzureRmWebApp -PhpVersion` als gültige PHP-Version eingestellt

## <a name="640---july-2018"></a>6.4.0 – Juli 2018
#### <a name="general"></a>Allgemein
* Formatierung von OutputType in Hilfedateien für die meisten Module korrigiert

#### <a name="azurermprofile"></a>AzureRM.Profile
* Attribut „Ps1Xml“ wurde den Standardausgabetypen hinzugefügt

#### <a name="azurermcompute"></a>AzureRM.Compute
* IP-Tag-Funktion für VMSS
    - Cmdlet „New-AzureRmVmssIpTagConfig“ hinzugefügt
    - IpTag-Parameter zu „New-AzureRmVmssIpConfig“ hinzugefügt
* Funktion für automatisches Betriebssystemrollback für VMSS
    - DisableAutoRollback-Parameter zu „New-AzureRmVmssConfig“ und „Update-AzureRmVmss“ hinzugefügt
* Funktion für Upgradeverlauf des Betriebssystems für VMSS
    - Switch-Parameter „OSUpgradeHistory“ zu „Get-AzureRmVmss“ hinzugefügt

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Unterstützung für Katalog-ACLs über die folgenden Befehle hinzugefügt:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Abbruchunterstützung und Nachverfolgung des Fortschritts für „Set-AzureRmDataLakeStoreItemAclEntry“, „Remove-AzureRmDataLakeStoreItemAclEntry“, „Set-AzureRmDataLakeStoreItemAcl“ hinzugefügt
* Abbruchunterstützung „Export-AzureRmDataLakeStoreChildItemProperties“ hinzugefügt
* Leerung von Debugmeldungen für Cmdlets korrigiert, die rekursive Vorgänge durchführt
* Speicherort des Test von DataLake-Cmdlets korrigiert

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Optionaler Parameter „MaxCount“ zu Listenvorgangs-Cmdlets „Get-AzureRmEventHub“ und „Get-AzureRmEventHubConsumerGroup“ hinzugefügt
* Problem in Cmdlet „New-AzureRmEventHub“ behoben, aufgrund dessen beim Erstellen einer neuen EventHub-Instanz mindestens ein Parameter benötigt wurde. Standardparametersatz wurde bereitgestellt.
* Optionaler Parameter“ -KeyValue“ zu Cmdlet „New-AzureRmEventHubKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Problem behoben, aufgrund dessen von „Get-AzureRmKeyVault -Tag“ alle Ressourcen zurückgegeben wurden.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Neue SKUs für zonenredundante VirtualNetworkGateways-Instanzen verfügbar gemacht
* Neue Befehle für Funktion hinzugefügt: ExpressRoute-Partner-APIs über ARM
    - Get-AzureRmExpressRouteCrossConnection hinzugefügt
    - Set-AzureRmExpressRouteCrossConnection hinzugefügt
    - Add-AzureRmExpressRouteCrossConnectionPeering hinzugefügt
    - Get-AzureRmExpressRouteCrossConnectionPeering hinzugefügt
    - Remove-AzureRmExpressRouteCrossConnectionPeering hinzugefügt
    - Get-AzureRMExpressRouteCrossConnectionArpTable hinzugefügt
    - Get-AzureRMExpressRouteCrossConnectionRouteTable hinzugefügt
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hinzugefügt

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Cmdlet „Get-AzureRmRecoveryServicesBackupStatus“ wurde hinzugefügt. Dieses Cmdlet überprüft anhand der ID eines virtuellen Computers, ob dieser durch einen Tresor im Abonnement geschützt ist. Wenn ein solcher Tresor vorhanden ist, gibt das Cmdlet die Tresordetails aus.

#### <a name="azurermresources"></a>AzureRM.Resources
* Cmdlets vom Typ „Get-AzureRmPolicyAssignment“ aktualisieren:
    - Unterstützung für das Auflisten von „-Scope“-Werten auf Verwaltungsgruppenebene hinzugefügt
    - Unterstützung für das Abrufen einzelner Arbeitsaufträge mit „-Scope“-Werten auf Verwaltungsgruppenebene hinzugefügt
    - Switches „-Effective“ und „-All“ zu Steuerparameter hinzugefügt
* Cmdlets vom Typ Get/New/Remove/Set-AzureRmPolicyDefinition aktualisiert
    - Parameter „-ManagementGroupName“ hinzugefügt, um Vorgänge auf eine bestimmte Verwaltungsgruppe anzuwenden
    - Parameter „-SubscriptionId“ hinzugefügt, um Vorgänge auf ein bestimmtes Abonnement anzuwenden
* Cmdlets vom Typ Get/New/Remove/Set-AzureRmPolicySetDefinition aktualisiert
    - Parameter „-ManagementGroupName“ hinzugefügt, um Vorgänge auf eine bestimmte Verwaltungsgruppe anzuwenden
    - Parameter „-SubscriptionId“ hinzugefügt, um Vorgänge auf ein bestimmtes Abonnement anzuwenden
* Unterstützung für KeyVault-Geheimnisverweis in Parametern hinzugefügt, wenn „TemplateParameterObject“ in „New-AzureRmResourceGroupDeployment“ verwendet wird
* Problem behoben, aufgrund dessen, der Parameter „-EndDate“ für „New-AzureRmADAppCredential“ ignoriert wurde
    - https://github.com/Azure/azure-powershell/issues/6505
* Problem behoben, aufgrund dessen „Add-AzureRmADGroupMember“ eine falsche URL für Anforderungen verwendete
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Optionaler Parameter“ -KeyValue“ zu Cmdlet „New-AzureRmServiceBusKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht.

#### <a name="azurermsql"></a>AzureRM.Sql
* Benutzerdefinierte Wiederherstellungspunkte für SQLDW in Hilfe zu „New-AzureRmSqlDatabaseRestorePoint“ erläutert
* Dokumentation von Parameter „-ComputeGeneration“ in mehreren Cmdlets aktualisiert

## <a name="630---june-2018"></a>6.3.0: Juni 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Aktualisierte Fehlermeldungen für „Enable-AzureRmContextAutoSave“
* Erstellen eines Kontexts für jedes Abonnement beim Ausführen von „Connect-AzureRmAccount“ ohne vorherigen Kontext

#### <a name="azurestorage"></a>Azure.Storage
* Zusätzliche Informationen zum Parameter „-Permissions“ in Hilfedateien

#### <a name="azurermcompute"></a>AzureRM.Compute
* „Get-AzureRmVmDiskEncryptionStatus“ behebt ein Problem, das bei virtuellen Computern ohne Datenträger festgestellt wurde. 
* Version der Computeclientbibliothek aktualisiert, um folgende Cmdlets zu korrigieren:
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Die folgenden Cmdlets wurden korrigiert, um die Vorgangs-ID und den Vorgangsstatus korrekt anzuzeigen:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* ValidateNotNullOrEmpty-Überprüfungskonditionen für „SubjectBeginsWith“/„SubjectEndsWith“ im Cmdlet „Update-AzureRmEventGridSubscription“ wurden entfernt, um bei Bedarf die Änderung dieser Parameter in eine leere Zeichenfolge zu ermöglichen.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Ein Problem wurde behoben, aufgrund dessen bei Ausführung von „Get-AzureRmKeyVault -Tag“ keine Tags zurückgegeben wurden.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Offizielle Veröffentlichung von Policy Insights-Cmdlets
    - Verwendung der API-Version 2018-04-04
    - „PolicyDefinitionReferenceId“ zu den Ergebnissen von „Get-AzureRmPolicyStateSummary“ hinzugefügt

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Parameter „-Vault“ zu den RecoveryServices.Backup-Cmdlets hinzugefügt. Bei der Übergabe wird dadurch das Cmdlet „Set-AzureRmRecoveryServicesContext“ außer Kraft gesetzt.

#### <a name="azurermsql"></a>AzureRM.Sql
* Aktualisiertes Beispiel in der Hilfedatei für „Get-AzureRmSqlDatabaseExpanded“

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Hilfedatei für „Add-AzureRmTrafficManagerEndpointConfig“ aktualisiert

#### <a name="azurermwebsites"></a>AzureRM.Websites
* „Set-AzureRmWebApp“ wurde aktualisiert, damit „AppSettings“ bei der Verwendung von „-AssignIdentity“ nicht außer Kraft gesetzt wird.
* „New-AzureRmWebAppSlot“ wurde aktualisiert, um „AppServicePlan“ als optionalen Parameter anzuerkennen

## <a name="621---june-2018"></a>6.2.1: Juni 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* PSWorkspace-Modell aktualisiert, damit das Netzwerk „type“ als Parameter verwenden kann

## <a name="620---june-2018"></a>6.2.0: Juni 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Beheben des Problems, aufgrund dessen Version 10.0.3 von Newtonsoft.Json beim Modulimport nicht geladen wurde

#### <a name="azurermcompute"></a>AzureRM.Compute
* Feature zum Aktualisieren von virtuellen VMSS-Computern
    - Cmdlets „Update-AzureRmVmssVM“ und „New-AzureRmVMDataDisk“ hinzugefügt
    - Fügen Sie den Parameter „VirtualMachineScaleSetVM“ zum Cmdlet „Add-AzureRmVMDataDisk“ hinzu, um das Hinzufügen eines Datenträgers zum virtuellen VMSS-Computer zu unterstützen.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Aktualisierung der ADF .Net SDK-Version auf 0.8.0-preview mit den folgenden Änderungen:
    - Vorgang zum Konfigurieren des Factoryrepositorys hinzugefügt
    - Der verknüpfte QuickBooks-Dienst wurde aktualisiert, um die Eigenschaften „consumerKey“ und „consumerSecret“ verfügbar zu machen.
    - Aktualisierung verschiedener Modelltypen von „SecretBase“ auf „Object“
    - Blobereignisauslöser hinzugefügt

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Aktualisierung der Dokumentation mit Beispielausgabe

### <a name="azurermnetwork"></a>AzureRM.Network
* Aktivierung der Traffic Analytics-Parameter für Network Watcher-Cmdlets

#### <a name="azurermresources"></a>AzureRM.Resources
* Behebung des Problems mit der Eigenschaft „Properties“ von PSResource-Objekten, die von „Get-AzureRmResource“ zurückgegeben wurden

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Behebung des Problems, dass beim Aktualisieren von „ServiceBusQueueJob“ keine neuen Authentifizierungswerte festgelegt wurden

### <a name="azurermsql"></a>AzureRM.Sql
* Aktualisierung der folgenden Cmdlets mit dem optionalen LicenseType-Parameter
    - New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* „New-AzureRMWebApp“ aktualisiert, um allgemeine Algorithmen aus der Strategiebibliothek zu verwenden.

## <a name="610---may-2018"></a>6.1.0 – Mai 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Behebung eines Problems, durch das beim Ausführen von „Clear-AzureRmContext“ ein leerer Kontext mit dem Namen des vorherigen Standardkontexts beibehalten wurde und der Benutzer dadurch keinen neuen Kontext mit dem alten Namen erstellen konnte

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Ermöglichung der Zuordnung von Gateways/Aufhebung der Gatewayzuordnung in AS

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Unterstützung für „ApiVersions“, „ApiReleases“ und „ApiRevisions“ hinzugefügt
* Unterstützung für ServiceFabric-Back-End hinzugefügt
* Unterstützung für Application Insights-Protokollierung hinzugefügt
* Unterstützung für die Erkennung von SKUs vom Typ „Basic“ als gültige SKU des API Management-Diensts hinzugefügt
* Unterstützung hinzugefügt, damit Zertifikate, die von der privaten Zertifizierungsstelle ausgestellt wurden, als Stamm- oder ZS-Zertifikate installiert werden können
* Unterstützung für die Akzeptierung benutzerdefinierter SSL-Zertifikate über KeyVault und mehrere Proxyhostnamen hinzugefügt
* Unterstützung für die verwaltete Dienstidentität hinzugefügt
* Unterstützung für die Annahme von Richtlinien über URL hinzugefügt; HINWEIS: Folgende Cmdlets werden in einem zukünftigen Release als veraltet gekennzeichnet:
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Veröffentlichung des neuen Cmdlets „Get-AzureBatchPoolNodeCounts“
* Veröffentlichung des neuen Cmdlets „Start-AzureBatchComputeNodeServiceLogUpload“

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Hinzufügung neuer Parameter („Expand“, „ResourceGroup“, „InstanceName“, „InstanceId“, „Tags“ und „Top“) für das Cmdlet „Get-AzureRmConsumptionUsageDetail“

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Korrektur des Beispiels für „Export AzureRmDataLakeStoreChildItemProperties“
* Korrektur der NULL-Parameterausnahme für rekursiven Fall in „Set-AzureRmDataLakeStoreItemAclEntry“ 
* Korrektur der Hilfedateien für „Set-AzureRmDataLakeStoreItemAclEntry“, „Set-AzureRmDataLakeStoreItemAcl“ und „Remove-AzureRmDataLakeStoreItemAclEntry“ 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Erhöhung der Network SDK-Version von 18.0.0-preview auf 19.0.0-preview
* Cmdlet zum Erstellen der Protokollkonfiguration hinzugefügt
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Cmdlet zum Hinzufügen einer neuen Leitungsverbindung zu einer vorhandenen ExpressRoute-Leitung hinzugefügt
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet zum Entfernen einer Leitungsverbindung aus einer vorhandenen ExpressRoute-Leitung hinzugefügt
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet zum Abrufen einer Leitungsverbindung hinzugefügt
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Verwendung der Serverauthentifizierung mit generierten Zertifikaten korrigiert (Problemnr. 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* Überwachungscmdlets korrigiert, um das Entfernen von „AuditActions“ oder „AuditActionGroups“ zu ermöglichen
* Problem mit „Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy“ behoben, das beim Festlegen einer neuen flexiblen Aufbewahrungsrichtlinie zu folgendem Fehler führte: „Configure long term retention policy with azure recovery service vault and policy is no longer supported. Please submit request with the new flexible retention policy“ (Das Konfigurieren einer langfristigen Aufbewahrungsrichtlinie mit Azure Recovery Service-Tresor und -Richtlinie wird nicht mehr unterstützt. Übermitteln Sie eine Anforderung mit der neuen flexiblen Aufbewahrungsrichtlinie.)
* Aktualisierung aller Cmdlets für Azure SQL-Datenbank, für die Erstellung von Pools für elastische Datenbanken und für die Aktualisierung, sodass sie die neue Datenbank-API verwenden. Diese unterstützt die Sku-Eigenschaft für skalierungs- und tarifbezogene Eigenschaften.
* Aktualisierte Cmdlets: 
    - New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Aktualisierung der Parameter für „Get-AzureRmTrafficManagerProfile“, sodass bei Verwendung des Parameters „-Name“ der Parameter „-ResourceGroupName“ erforderlich ist
