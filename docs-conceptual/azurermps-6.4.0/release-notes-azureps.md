---
title: Azure PowerShell-Änderungsprotokoll | Microsoft-Dokumentation
description: Hierbei handelt es sich um einen Verlauf der Änderungen, die in der neuesten Version an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406293"
---
# <a name="release-notes"></a>Versionshinweise

Hierbei handelt es sich um eine Liste der Änderungen, die in dieser Version an Azure PowerShell vorgenommen wurden.

---
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