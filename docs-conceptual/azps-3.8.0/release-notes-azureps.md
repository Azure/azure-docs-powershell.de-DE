---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "82080197"
---
# <a name="azure-powershell-release-notes"></a>Versionshinweise zu Azure PowerShell

## <a name="380---april-2020"></a>3.8.0: April 2020
### <a name="highlights-since-the-last-release"></a>Highlights seit dem letzten Release
* Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7

#### <a name="azaccounts"></a>Az.Accounts
* Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]

#### <a name="azapimanagement"></a>Az.ApiManagement
* Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt
* „Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert

#### <a name="azcdn"></a>Az.Cdn
* Anzeige der Preis-SKU für ChinaCDN korrigiert

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“

#### <a name="azcompute"></a>Az.Compute
* Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt
* „Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.

#### <a name="aziothub"></a>Az.IotHub
* Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:
    - Get-AzIotHubDeviceTwin
    - Update-AzIotHubDeviceTwin
* Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.
* Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:
    - Get-AzIotHubModuleTwin
    - Update-AzIotHubModuleTwin
* Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil. Die folgenden Cmdlets sind neu:
    - Add-AzIotHubConfiguration
    - Get-AzIotHubConfiguration
    - Remove-AzIotHubConfiguration
    - Set-AzIotHubConfiguration
* Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.

#### <a name="azkeyvault"></a>Az.KeyVault
* Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.
* Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]
* Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]
* Unterstützung zu privatem Endpunkt hinzugefügt

#### <a name="azmaintenance"></a>Az.Maintenance
* Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets

#### <a name="azmonitor"></a>Az.Monitor
* Cmdlets für Private Link-Bereich hinzugefügt
    - Get-AzInsightsPrivateLinkScope
    - Remove-AzInsightsPrivateLinkScope
    - New-AzInsightsPrivateLinkScope
    - Update-AzInsightsPrivateLinkScope
    - Get-AzInsightsPrivateLinkScopedResource
    - New-AzInsightsPrivateLinkScopedResource
    - Remove-AzInsightsPrivateLinkScopedResource

#### <a name="aznetwork"></a>Az.Network
* Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen
    - New-AzVirtualNetworkGateway
    - Set-AzVirtualNetworkGateway
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection
* Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert
    - New-AzLocalNetworkGateway
    - New-AzVpnSiteLink
* Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt
    - „Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt
        - Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties
    - „Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert
        - Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt
* Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt
* Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert

#### <a name="azsql"></a>Az.Sql
* Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt
* Unterstützte Überwachung eines Speicherkontos im VNET

#### <a name="azstorage"></a>Az.Storage
* Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt
* Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos
    - New-AzStorageAccount
    - Set-AzStorageAccount
* Unterstützung für DataLake Gen2
    - New-AzDataLakeGen2Item
    - Get-AzDataLakeGen2Item
    - Get-AzDataLakeGen2ChildItem
    - Move-AzDataLakeGen2Item
    - Set-AzDataLakeGen2ItemAclObject
    - Update-AzDataLakeGen2Item
    - Get-AzDataLakeGen2ItemContent
    - Remove-AzDataLakeGen2Item

## <a name="0100-preview---april-2020"></a>0.10.0-preview: April 2020
### <a name="general"></a>Allgemein
* Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar. Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs. Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).
* Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.
* Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.
* Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).

## <a name="370---march-2020"></a>3.7.0: März 2020
#### <a name="azaccounts"></a>Az.Accounts
* „Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]

#### <a name="azcompute"></a>Az.Compute
* Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen
* Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben [Nr. 11354]
* Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:
    - Set-AzVMAEMExtension
    - Get-AzVMAEMExtension
    - Remove-AzVMAEMExtension
    - Update-AzVMAEMExtension
* Fehler in Beispielen im Hilfedokument korrigiert
* Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.
* New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist [Nr. 11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 4.8.0 aktualisiert
* Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt
* Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt

#### <a name="azhdinsight"></a>Az.HDInsight
* Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt

#### <a name="aziothub"></a>Az.IotHub
* Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt Die folgenden Cmdlets sind neu:
    - Get-AzIotHubDistributedTracing
    - Set-AzIotHubDistributedTracing

#### <a name="azkeyvault"></a>Az.KeyVault
* Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt

#### <a name="azmonitor"></a>Az.Monitor
* Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert

#### <a name="aznetwork"></a>Az.Network
* Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen
    - New-AzVirtualHubVnetConnection
    - Update-AzVirtualHubVnetConnection
    - New-AzVirtualHub
    - Update-AzVirtualHub
* Abhängigkeit vom SQL Management SDK entfernt

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Verbesserte Fehlermeldungen

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert
* Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt
* Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt
* Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt
* Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt
* Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt

#### <a name="azresources"></a>Az.Resources
* „Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]
* Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt
* Kleine Änderung an der Dokumentation für „Get-AzResourceLock“ Beispiel hinzugefügt
* Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]
* Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt

#### <a name="azsql"></a>Az.Sql
* Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt
* Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt
* Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert

#### <a name="azsupport"></a>Az.Support
* Allgemeine Verfügbarkeit des Moduls „Az.Support“

#### <a name="azwebsites"></a>Az.Websites
* Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:
    - Get-AzWebAppTrafficRouting
    - Update-AzWebAppTrafficRouting
    - Add-AzWebAppTrafficRouting
    - Remove-AzWebAppTrafficRouting

## <a name="361---march-2020"></a>3.6.1 – März 2020
#### <a name="azaccounts"></a>Az.Accounts
* Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]
* Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]
* Az-Version in UserAgent hinzugefügt

#### <a name="azapimanagement"></a>Az.ApiManagement
* Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]
* „Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]
* „Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt
* „New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.

#### <a name="aziothub"></a>Az.IotHub
* Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt Die folgenden Cmdlets sind neu:
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice
* Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt. Die folgenden Cmdlets sind neu:
    - „Add-AzIotHubModule“
    - „Get-AzIotHubModule“
    - „Remove-AzIotHubModule“
    - „Set-AzIotHubModule“
* Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.
* Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.
* Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt. Die folgenden Cmdlets sind neu:
    - „Get-AzIotHubDeviceParent“
    - „Set-AzIotHubDeviceParent“
* Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.

#### <a name="azmonitor"></a>Az.Monitor
* Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]

#### <a name="aznetwork"></a>Az.Network
* SQL Management SDK aktualisiert.
* Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.
    - Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.
* PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben
* Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]
* Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]
* Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]
* Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben
* Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.
* „Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.
* Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Neues Tag-Cmdlet hinzugefügt
    - Update-AzTag -ResourceId
* ScopedDeployment aus SDK 3.3.0 übernommen

#### <a name="azsql"></a>Az.Sql
* Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.
* Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt
    - Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank
    - Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort
    - Entfernen einer LTR-Sicherung
    - Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank
* MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt
* MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt
* SQL SDK-Version für Az.Network festgelegt

#### <a name="azstorage"></a>Az.Storage
* Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy
    - „Set-AzRmStorageContainerImmutabilityPolicy“
* Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version
    - „New-AzStorageTable“
    - „Get-AzStorageTable“

#### <a name="azwebsites"></a>Az.Websites
* Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt
* Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird
* Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden
* Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet
* Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben

## <a name="350---february-2020"></a>3.5.0: Februar 2020
### <a name="highlights-since-the-last-major-release"></a>Highlights seit der letzten Hauptversion
* Clientseitige Telemetrie aktualisiert
* Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt
* Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt

#### <a name="azaccounts"></a>Az.Accounts
* Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt

#### <a name="azautomation"></a>Az.Automation
* Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* SDK auf 7.0 aktualisiert
* Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet

#### <a name="azcompute"></a>Az.Compute
* Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können

#### <a name="aziothub"></a>Az.IotHub
* Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt Die folgenden Cmdlets sind neu:
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice

#### <a name="azkeyvault"></a>Az.KeyVault
* Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert

#### <a name="azmonitor"></a>Az.Monitor
* Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert
* Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.
    - Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.

#### <a name="aznetwork"></a>Az.Network
* Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt
* FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert
* Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt
* Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls
    - Keine neuen Cmdlets hinzugefügt. Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Cmdlets für die Vorlagenbereitstellung umgestaltet
    - Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: *-AzManagementGroupDeployment
    - Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: *-AzTenantDeployment
    - Cmdlets vom Typ „*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet
    - Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt
* „Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird
* „ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden
* Hilfedateien erneut generiert

#### <a name="azsql"></a>Az.Sql
* Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt
* Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt
* Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt

#### <a name="azstoragesync"></a>Az.StorageSync
* Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert

## <a name="340---february-2020"></a>3.4.0: Februar 2020
### <a name="highlights-since-the-last-major-release"></a>Highlights seit der letzten Hauptversion
* Az.CosmosDB: erste Version 0.1.0 veröffentlicht
* Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt

#### <a name="azaccounts"></a>Az.Accounts
* Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist
* Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct*** und **Set-AzApiManagementProduct**
  - Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht

#### <a name="azcompute"></a>Az.Compute
* Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird
* Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt
* Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 4.7.0 aktualisiert

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* LIST-Vorgänge für Ressourcen hinzugefügt
* Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt

#### <a name="azhdinsight"></a>Az.HDInsight
* Dokumentationsfehler für „New-AzHDInsightCluster“ behoben

#### <a name="azkeyvault"></a>Az.KeyVault
* Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen

#### <a name="aznetwork"></a>Az.Network
* Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen
* Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden
    - New-AzFirewall-Cmdlet aktualisiert:
        - Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert
        - Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.
* Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen
* Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte
* Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt
    - Neu hinzugefügte Cmdlets:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen
    - Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt
* Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt
* „Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers
* In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.

#### <a name="azresources"></a>Az.Resources
* „-Scope“ in Cmdlets vom Typ „*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)
* Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt

#### <a name="azsql"></a>Az.Sql
Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen

#### <a name="azstorage"></a>Az.Storage
* Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos
    - New-AzStorageAccount
* Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen
* Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert

#### <a name="azwebsites"></a>Az.Websites
* „Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.
* Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.

## <a name="330---january-2020"></a>3.3.0 – Januar 2020
#### <a name="azaccounts"></a>Az.Accounts
* „Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.

#### <a name="azcdn"></a>Az.Cdn
* Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“

#### <a name="azcompute"></a>Az.Compute
* Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt
  - Edge-Speichercontainer abrufen
* Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt
  - Neuen Edge-Speichercontainer erstellen
* Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt
  - Edge-Speichercontainer entfernen
* Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt
  - Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen
* Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt
  - Edge-Speicherkonto abrufen
* Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt
  - Neues Edge-Speicherkonto erstellen
* Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt
  - Edge-Speicherkonto entfernen
* Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen
  - Aktion zum Aktualisieren von Daten auf Freigabe aufrufen
* Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt
  - Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“

#### <a name="azdatafactory"></a>Az.DataFactory
* Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt
* Version des ADF .NET SDK auf 4.6.0 aktualisiert
* Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt

#### <a name="azeventhub"></a>Az.EventHub
* Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert

#### <a name="azhdinsight"></a>Az.HDInsight
* Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind
* Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure
* Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure
* Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure

#### <a name="azresources"></a>Az.Resources
* Fehler in Hilfedokument zu „Remove-AzTag“ behoben

#### <a name="azsql"></a>Az.Sql
* Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.
* Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* DR als neuer gültiger Lizenztyp hinzugefügt

#### <a name="azstorage"></a>Az.Storage
* Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version
    - Update-AzStorageAccountNetworkRuleSet
* Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0: Dezember 2019

### <a name="general"></a>Allgemein
* Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert

#### <a name="azaccounts"></a>Az.Accounts
* Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt
* Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist

#### <a name="azbatch"></a>Az.Batch
* Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 4.5.0 aktualisiert

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt
* SocketAddr zur automatischen Vervollständigung hinzugefügt

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Ausnahmebehandlung

#### <a name="azkeyvault"></a>Az.KeyVault
* Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben
* Zertifikatverwaltung für Kryptografie für elliptische Kurve
    - Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt

#### <a name="azmonitor"></a>Az.Monitor
* Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt. Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als dedizierter Datentyp)

#### <a name="aznetwork"></a>Az.Network
* Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln

#### <a name="azresources"></a>Az.Resources
* Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht
* Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt

#### <a name="azsql"></a>Az.Sql
* Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert

#### <a name="azstorage"></a>Az.Storage
* Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden
    - Revoke-AzStorageAccountUserDelegationKeys
* Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen
* Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt
    - Set-AzStorageShareQuota
* Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 – November 2019
### <a name="highlights-since-the-last-major-release"></a>Highlights seit der letzten Hauptversion
* Az.DataBoxEdge 1.0.0 veröffentlicht
* Az.SqlVirtualMachine 1.0.0 veröffentlicht

#### <a name="azcompute"></a>Az.Compute
* Funktion zum erneuten Anwenden von VMs
    - Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt
* AutomaticRepairs-Funktion für VM-Skalierungsgruppe:
    - Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss
* Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“
* „Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt
* Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt
* Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert
* Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt
* Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt
* Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt
    - Bestellung abrufen
* Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt
    - Neue Bestellung erstellen
* Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt
    - Bestellung entfernen
* Änderung im Cmdlet `New-AzDataBoxEdgeShare`
    - Erstellt jetzt eine lokale Freigabe
* Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt
    - „IotRole“ kann jetzt einer Freigabe zugeordnet werden.
* Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt
    - Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren
* Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt
    - Ruft die Informationen zu Auslösern ab
* Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt
    - Neue Auslöser erstellen
* Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt
    - Auslöser entfernen

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 4.4.0 aktualisiert
* Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert

#### <a name="azeventhub"></a>Az.EventHub
* Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt
* Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt
* Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.

#### <a name="azprivatedns"></a>Az.PrivateDns
* PrivateDns.net-SDK auf Version 1.0.0 aktualisiert

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.
* Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.
* SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.

#### <a name="azrediscache"></a>Az.RedisCache
* Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt. Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.
* Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt

#### <a name="azresources"></a>Az.Resources
- Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.
- Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert
- Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.
- Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.
- „New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.

#### <a name="azsql"></a>Az.Sql
* Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.
* Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt

## <a name="300---november-2019"></a>3.0.0 – November 2019
### <a name="general"></a>Allgemein
* Az.PrivateDns 1.0.0 veröffentlicht.

#### <a name="azaccounts"></a>Az.Accounts
* Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.

#### <a name="azadvisor"></a>Az.Advisor
* Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.

#### <a name="azbatch"></a>Az.Batch
* `CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt. Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.
  - Dies wirkt sich auf **Get-AzBatchAccount** aus.
* Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.
* Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten. Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.
  - Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:
    - Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.
    - Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.
* `ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.
  - Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden. Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* `ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.
  - `ApplicationId` ist jetzt ein Alias von `ApplicationName`.
* Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.
* `Version` für `PSApplicationPackage` in `Name` umbenannt.
* `BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.
* `OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.
* **Set-AzBatchPoolOSVersion** entfernt. Dieser Vorgang wird nicht mehr unterstützt.
* `TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.
* `CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.
* `DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.
* **Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.
  - **Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.
  - Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben. Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.
* Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.
* Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren. Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.
* Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe. Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.
* Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt. So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.
* Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).
* Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).

#### <a name="azcdn"></a>Az.Cdn
* „UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.
* Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.

#### <a name="azcompute"></a>Az.Compute
* Feature „Datenträgerverschlüsselungssatz“
    - Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
    - Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig
* Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.
* „FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.
* „ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.
* Aktuelle Änderungen
    - Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.
    - Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 4.3.0 aktualisiert.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:
* Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann
* Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“
* Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung
* Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort
* Behebung eines Verkettungsfehlers

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Verschiedene Tippfehler im Modul korrigiert.

#### <a name="azhdinsight"></a>Az.HDInsight
* Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.
* Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.
* Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.
* Fünf Cmdlets wurden entfernt:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Drei Cmdlets wurden hinzugefügt:
    - „Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.
    - „Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.
    - „Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.
* Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.
* Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.
* Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.
* Der Ausgabetyp der folgenden Cmdlets wurde geändert:
*  - Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.
*  - Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.
*  - Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.
* Einige Testfälle für Szenarien wurden hinzugefügt.
* Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.

#### <a name="aziothub"></a>Az.IotHub
* Wichtige Änderungen:
    - Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
    - Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.
    - Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
    - Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.
    - Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.
    - Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.
    - Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.
    - Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.
    - Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
    - Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.
    - Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
    - Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.
* Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.
* Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.
* Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.
* Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.
* Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.
* Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.
* Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.
* Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.

#### <a name="azresources"></a>Az.Resources
* Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.

#### <a name="aznetwork"></a>Az.Network
* Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.
    - Aktualisiertes Cmdlet:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.
    - Neues Cmdlet:
        - Get-AzPrivateLinkResource
* Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.
    - „EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.
    - „LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.
    - „New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.
* Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.
* Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.
* Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.
    - Neu hinzugefügte Cmdlets:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.
    - Mit optionalen Parametern aktualisierte Cmdlets:
        - New-AzVirtualHub: Parameter „Sku“ hinzugefügt.
        - Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.
        - New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.
        - Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.
* Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.
    - Neu hinzugefügte Cmdlets:
        - Update-AzureRmVirtualHubVnetConnection
    - Mit optionalen Parametern aktualisierte Cmdlets:
        - New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.
        - New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.
        - Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.
        - New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.
        - Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.
* Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.
    - Neu hinzugefügte Cmdlets:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Mit optionalen Parametern aktualisierte Cmdlets:
        - New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.
* Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.
    - „GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.
* Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.
    - Mit optionalen Parametern aktualisierte Cmdlets:
        - New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.
        - New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.
* Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.
* Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.
* Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.
    - Neu hinzugefügte Cmdlets:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.

#### <a name="azsql"></a>Az.Sql
* Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.
* Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.
* Veraltete Aliase entfernt:
* Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)
* Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)
* Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.
* Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.
* Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.
* Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.

#### <a name="azstorage"></a>Az.Storage
* Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

## <a name="280---october-2019"></a>2.8.0: Oktober 2019
### <a name="general"></a>Allgemein
* Az.HealthcareApis-Release 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt
    - Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert

#### <a name="azbatch"></a>Az.Batch
* **Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.

#### <a name="azcompute"></a>Az.Compute
* Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt
* Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert
* Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert
* Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)

#### <a name="azdatafactory"></a>Az.DataFactory
* CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow
* Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession
* Version des ADF .NET SDK auf 4.2.0 aktualisiert

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* PowerShell-Version auf 1.0.0 aktualisiert
* SDK-Version auf 1.0.2 aktualisiert
* Aktualisierung in Tests, um auf neue SDK-Version zu verweisen
* Ausgabestruktur von geschachtelt in vereinfacht geändert

#### <a name="aziothub"></a>Az.IotHub
* Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents
* Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.

#### <a name="azmonitor"></a>Az.Monitor
* Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert. Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.
* Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.

#### <a name="aznetwork"></a>Az.Network
* Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können
* Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt
    - Neu hinzugefügte Cmdlets:
        - New-AzureRmTrafficSelectorPolicy
    - Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
* Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt
    - Aktualisierte Cmdlets:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets
* Neue Generationen und SKUs für VirtualNetworkGateways
  - Einführung neuer Generationen für VirtualNetworkGateways
  - Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways

#### <a name="azrediscache"></a>Az.RedisCache
* Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen

#### <a name="azsql"></a>Az.Sql
* Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt

#### <a name="azstorage"></a>Az.Storage
* Storage-Clientbibliothek auf 11.1.0 aktualisiert
* Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet
    -  Get-AzRmStorageContainer
* Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben

#### <a name="azwebsites"></a>Az.Websites
* Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“

## <a name="270---september-2019"></a>2.7.0: September 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert
* Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt. Verwenden Sie stattdessen „Set-AzApiManagement“.

#### <a name="azautomation"></a>Az.Automation
* Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert
* Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt
* Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.

#### <a name="azcompute"></a>Az.Compute
* Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt
* Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt
* Feature für VM mit niedriger Priorität hinzugefügt:
    - Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt
    - Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt
* Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden
* Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert
* VHD-Suchmethode für Position relativ zum Ende korrigiert
* Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben

#### <a name="azdatafactory"></a>Az.DataFactory
* Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus
* Version des ADF .NET SDK auf 4.1.3 aktualisiert

#### <a name="azhdinsight"></a>Az.HDInsight
* Hinweis auf Breaking Changes hinzugefügt

#### <a name="aziothub"></a>Az.IotHub
* Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt
* Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt Die folgenden Cmdlets sind neu:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview
   - Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte. Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.
   - Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**). Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.
   - Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**. Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt. **HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.
   - Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert. Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.
   - Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert. Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.
* Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2
    - New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.
    - Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.
* Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)
 - Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)
 - Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt
 - Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt
 - Hilfedateien insgesamt verbessert
* Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben

#### <a name="aznetwork"></a>Az.Network
* Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert
* Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt
* Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten
* Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen
* Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten
* Falsche Zuordnung der Sicherheitsregelmodelle korrigiert
* Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt
    - Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt
    - Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt
    - Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt
* Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt
* Unterstützung von Mehrfachverbindungen in Virtual WAN
    - Neue Cmdlets
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Aktualisiertes Cmdlet:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert
* Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert
* Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet

#### <a name="azsignalr"></a>Az.SignalR
* Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt

#### <a name="azsql"></a>Az.Sql
* Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert
* V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)
* Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist
* Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen
* Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)

#### <a name="azstorage"></a>Az.Storage
* Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert
* Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben
    -  Set-AzStorageBlobContent
* Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden
* „Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert
* Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert

## <a name="260---august-2019"></a>2.6.0: August 2019
#### <a name="general"></a>Allgemein
* Verschiedene Tippfehler in zahlreichen Modulen korrigiert

#### <a name="azaccounts"></a>Az.Accounts
* Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)

#### <a name="azaks"></a>Az.Aks
* Problem mit der Ausgabe für „Get-AzAks“ behoben
    * Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351
    - .NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt
* **Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752
* Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer

#### <a name="azbatch"></a>Az.Batch
* Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)

#### <a name="azcdn"></a>Az.Cdn
* Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert

#### <a name="azcompute"></a>Az.Compute
* VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt
* Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt
* HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt
* Host- und HostGroup-Features hinzugefügt
    - Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost
    - Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt
* Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert
* Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert

#### <a name="azdatafactory"></a>Az.DataFactory
* Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)
* Version des ADF .NET SDK auf 4.1.2 aktualisiert
* Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen
* „PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben

#### <a name="azeventhub"></a>Az.EventHub
* Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“
* Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.
* Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt
* Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert

#### <a name="azmonitor"></a>Az.Monitor
* Falscher Parametername in der Hilfedokumentation korrigiert

#### <a name="aznetwork"></a>Az.Network
* „New-AzPrivateLinkServiceIpConfig“ aktualisiert
    - Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde
    - Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht
* Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.
* Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird
* „Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt
* Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“
    - Beispiel hinzugefügt
    - Beschreibung für den Parameter „-Name“ aktualisiert
* Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt
* Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* „Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert

#### <a name="azresources"></a>Az.Resources
* Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt
    - Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt
    - Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.
* Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt

#### <a name="azservicebus"></a>Az.ServiceBus
* Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“
* Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen
* Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:
    - Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen Problembehebung: https://github.com/Azure/azure-powershell/issues/8681
    - Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster Problembehebung: https://github.com/Azure/azure-powershell/issues/8407
    - Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert

#### <a name="azsql"></a>Az.Sql
* Dokumentation alter Überwachungs-Cmdlets aktualisiert

#### <a name="azstorage"></a>Az.Storage
* Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)
* Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Unterstützung der Aktivierungspriorität im Kopierblob
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“

## <a name="250---july-2019"></a>2.5.0: Juli 2019
#### <a name="azaccounts"></a>Az.Accounts
* Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert

#### <a name="azautomation"></a>Az.Automation
* Tippfehler in der Ressourcenzeichenfolge korrigiert

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Unterstützung für NetworkRuleSet hinzugefügt

#### <a name="azcompute"></a>Az.Compute
* Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 4.1.0 aktualisiert
* Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert

#### <a name="azeventhub"></a>Az.EventHub
* Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken
* Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird

#### <a name="azkeyvault"></a>Az.KeyVault
* Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt

#### <a name="azlogicapp"></a>Az.LogicApp
* Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen
    - Neuer MapType-Parameter für Filterung hinzugefügt

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt

#### <a name="aznetwork"></a>Az.Network
* Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt
    - Neue Cmdlets
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork
    - „New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert
        - Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen
        - Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen
* Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.
* ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert
    - Aktualisierte Cmdlets
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt
* PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt
    - Aktualisiertes Cmdlet:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert
    - „New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird. Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert
* Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* „Get-AzRecoveryServicesBackupJob.md“ aktualisiert
* „Get-AzRecoveryServicesBackupContainer.md“ aktualisiert
* „Get-AzRecoveryServicesVault.md“ aktualisiert
* „Wait-AzRecoveryServicesBackupJob.md“ aktualisiert
* „Set-AzRecoveryServicesVaultContext.md“ aktualisiert
* „Get-AzRecoveryServicesBackupItem.md“ aktualisiert
* „Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert
* „Restore-AzRecoveryServicesBackupItem.md“ aktualisiert
* Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert
* „Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert

#### <a name="azresources"></a>Az.Resources
- Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird
- Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert

#### <a name="azservicebus"></a>Az.ServiceBus
* Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken
* Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird

#### <a name="azsql"></a>Az.Sql
* Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert
* Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert
* Tippfehler in einer Warnmeldung korrigiert

#### <a name="azstorage"></a>Az.Storage
* Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird

#### <a name="azstoragesync"></a>Az.StorageSync
* Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt
* Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben

#### <a name="azwebsites"></a>Az.Websites
* Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden
* Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt
* Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben

## <a name="240---july-2019"></a>2.4.0 – Juli 2019
#### <a name="azaccounts"></a>Az.Accounts
* Unterstützung für Profil-Cmdlets hinzugefügt
* Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt
* Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde

#### <a name="azadvisor"></a>Az.Advisor
* Allgemein verfügbares Release von Az.Advisor
* Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.

#### <a name="azapimanagement"></a>Az.ApiManagement
* Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt
        - Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“
* Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt

#### <a name="azautomation"></a>Az.Automation
* Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben

#### <a name="azcompute"></a>Az.Compute
* Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt

#### <a name="azdatafactory"></a>Az.DataFactory
* Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen

#### <a name="azeventgrid"></a>Az.EventGrid
* Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben

#### <a name="aziothub"></a>Az.IotHub
* Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt

#### <a name="aznetwork"></a>Az.Network
* „RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt
* Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Fehlerbehebung für Nullverweis in Get-AzPolicyState
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Fehlerbehebung für Befehl „get-policy“ IaaSVMs

#### <a name="azresources"></a>Az.Resources
    - Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert
    - Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt
    - Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt
    - Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets

#### <a name="azservicebus"></a>Az.ServiceBus
* Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück

#### <a name="azsql"></a>Az.Sql
* Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt
* Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt

#### <a name="azstorage"></a>Az.Storage
* Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:
    -  Enable-AzStorageStaticWebsite
* Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt
* Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“
* Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.

## <a name="232---june-2019"></a>2.3.2 – Juni 2019
#### <a name="azaccounts"></a>Az.Accounts
* Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983
* Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.
* Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben

#### <a name="azdns"></a>Az.Dns
* Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben

#### <a name="azeventgrid"></a>Az.EventGrid
* Zur Verwendung der API-Version 2019-06-01 aktualisiert
* Neue Cmdlets:
    - New-AzureRmEventGridDomain
        - Erstellt eine neue Azure Event Grid-Domäne.
    - Get-AzureRmEventGridDomain
        - Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.
    - Remove-AzureRmEventGridDomain
        - Entfernt eine Azure Event Grid-Domäne.
    - New-AzureRmEventGridDomainKey
        - Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.
    - Get-AzureRmEventGridDomainKey
        - Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.
    - New-AzureRmEventGridDomainTopic:
        - Erstellt ein neues Azure Event Grid-Domänenthema.
    - Get-AzureRmEventGridDomainTopic
        - Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.
    - Remove-AzureRmEventGridDomainTopic:
        - Entfernt ein vorhandenes Azure Event Grid-Domänenthema.
* Aktualisierte Cmdlets:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen
        - Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen
        - Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)
        - Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:
            - Ablaufdatum des Ereignisabonnements
            - Erweiterte Filterparameter
        - Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt
        - Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt
    - Remove-AzureRmEventGridSubscription
        - Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen
        - Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt
* New-AzFrontDoorWafManagedRuleObject
    - Neue Werte für automatisches Vervollständigen hinzugefügt

#### <a name="aznetwork"></a>Az.Network
* Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt
    - Neue Cmdlets
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* AvailablePrivateEndpointType
    - Neue Cmdlets
        - Get-AzAvailablePrivateEndpointType
* „PrivatePrivateLinkService“ hinzugefügt
    - Neue Cmdlets
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* „PrivateEndpoint“ hinzugefügt
    - Neue Cmdlets
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“
    - „New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll
    - „Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll
* Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt
* Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt
* Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen
* Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben
* Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte
* Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben
* Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert
* Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)
* Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt
* Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt
* Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt
    - New-AzFirewall-Cmdlet aktualisiert:
        - Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert
        - Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert
        - Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)
        - Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert
* Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt
    - „New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt
    - „Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.
    - „Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren

#### <a name="azresources"></a>Az.Resources
* Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt
    - Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt
    - Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt
    - Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)

#### <a name="azsql"></a>Az.Sql
* Suffix des Advanced Threat Protection-Endpunkts korrigiert
* Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert
* Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos
    - New-AzStorageAccount
* Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)
* Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt

## <a name="220---june-2019"></a>2.2.0 – Juni 2019
#### <a name="azcdn"></a>Az.Cdn
* Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.

#### <a name="azcompute"></a>Az.Compute
* Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.
    - Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück
* Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück

#### <a name="aznetwork"></a>Az.Network
* ResourceId und InputObject wurden für NAT Gateway aktualisiert
    - Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Fehlerbehebung für Nullverweis in Get-AzPolicyEvent

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert

#### <a name="azservicebus"></a>Az.ServiceBus
* Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben
* Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben

#### <a name="azsql"></a>Az.Sql
* Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen
* Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt
* Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt
* New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional

#### <a name="azwebsites"></a>Az.Websites
* Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben

## <a name="210---may-2019"></a>2.1.0 – Mai 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt
    - **Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde
    - **New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich
    - **New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text
    - **New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway
    - **New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose
    - **Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich
    - **Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich
* Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt
    - **Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches
    - **New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure
    - **Remove-AzApiManagementCache**: Entfernen eines Caches
    - **Update-AzApiManagementCache**: Aktualisieren eines Caches
* Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt
    - **New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API
    - **Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas
    - **Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas
    - **Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas
* Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt
    - **New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./
* Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt
    - **Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.
* Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert
    - Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt
    - Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt
    - Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“ Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren
    - Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt
* Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen
* Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]
* Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert
* Cmdlet **Import-AzApiManagementApi** wurde aktualisiert
    - Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation
    - Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist
    - Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist
* Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben
* Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben
* Cmdlet **New-AzApiManagementApi** wurde aktualisiert
    - Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver
    - Zum Erstellen einer API in einem „ApiVersionSet“
    - Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“
    - Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich
* Cmdlet **Set-AzApiManagementApi** wurde aktualisiert
    - Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver
    - Zum Aktualisieren einer API in einem „ApiVersionSet“
    - Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich
* Cmdlet **New-AzApiManagementRevision** wurde aktualisiert
    - Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“ Die neue Version übernimmt die „ApiId“ des übergeordneten Elements
    - Zum Bereitstellen einer „ApiRevisionDescription“
    - Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API
* Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert
    - Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“
    - Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“
* Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert
    - Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“
    - Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“
    - Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt
* Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert
    - Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“
    - Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“
    - Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt
* Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren
    - 'New-AzApiManagementContext'
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - 'Get-AzApiManagementApiRelease'
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - 'Get-AzApiManagementApiVersionSet'
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - 'Get-AzApiManagementAuthorizationServer'
    - 'Get-AzApiManagementBackend'
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - 'Get-AzApiManagementCertificate'
    - 'Remove-AzApiManagementApiVersionSet'
    - 'Remove-AzApiManagementSubscription'

#### <a name="azautomation"></a>Az.Automation
* Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.
    - Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977
    - Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600
* Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten
    * Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347
* Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt Jetzt wird nur der übereinstimmende Knoten zurückgegeben

#### <a name="azcompute"></a>Az.Compute
* Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt
* Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert

#### <a name="azmonitor"></a>Az.Monitor
* Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen

#### <a name="aznetwork"></a>Az.Network
* DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt
    - Aktualisiertes Cmdlet:
        - Get-AzEffectiveRouteTable
* Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate

#### <a name="azresources"></a>Az.Resources
* Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt

#### <a name="azsql"></a>Az.Sql
* „Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren

## <a name="200---may-2019"></a>2.0.0: Mai 2019
#### <a name="azaccounts"></a>Az.Accounts
* Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste
* Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte

#### <a name="azcompute"></a>Az.Compute
* Feature für die Näherungsplatzierungsgruppe
    - Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.
* „TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.
* Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.
* Aktuelle Änderungen
    - „Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert
    - „Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets

#### <a name="azdns"></a>Az.Dns
* Automatische Delegierung des DNS-Namenservers
    - Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.
    - NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets
* WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Zwei Cmdlets entfernt:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen
* Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:
    - Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.
    - Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.

#### <a name="azmonitor"></a>Az.Monitor
* Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API
    - „Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen

#### <a name="aznetwork"></a>Az.Network
* Unterstützung für NAT-Gatewayressource hinzugefügt
    - Neue Cmdlets
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Aktualisierte Cmdlets
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt
    - „New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.
    - „Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Unterstützung für die Abfrage von Richtlinienauswertungsdetails
    - Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt Unterstützung für „-Expand PolicyEvaluationDetails“

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung
* Markierung anstehender wichtiger Änderungen für Azure Site Recovery
* Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan
* Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure
* Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger
* Weitere kleinere Korrekturen

#### <a name="azrelay"></a>Az.Relay
* Korrektur von Tippfehlern in Kundennachrichten

#### <a name="azservicebus"></a>Az.ServiceBus
* Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt

#### <a name="azstorage"></a>Az.Storage
* Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)
* Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen
* Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert
    - New-AzStorageAccount
* Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.
* „Get-AzWebApp*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert

## <a name="180---april-2019"></a>1.8.0: April 2019
### <a name="highlights-since-the-last-major-release"></a>Highlights seit der letzten Hauptversion
* Allgemeine Verfügbarkeit des `Az`-Moduls
* Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.
* Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.
* Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt
* Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt
* Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt
* Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration

#### <a name="azaccounts"></a>Az.Accounts
* „Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen

#### <a name="azbatch"></a>Az.Batch
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azcdn"></a>Az.Cdn
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azcompute"></a>Az.Compute
* Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.
* Dokumentation für Platzhalter korrigiert

#### <a name="azdatafactory"></a>Az.DataFactory
* „SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azeventgrid"></a>Az.EventGrid
* Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden

#### <a name="azeventhub"></a>Az.EventHub
* Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt

#### <a name="azhdinsight"></a>Az.HDInsight
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="aziothub"></a>Az.IotHub
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azkeyvault"></a>Az.KeyVault
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.
* Dokumentation für Platzhalter korrigiert

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azmedia"></a>Az.Media
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azmonitor"></a>Az.Monitor
  * Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Monitor SDK auf Version 0.22.0-preview aktualisiert

#### <a name="aznetwork"></a>Az.Network
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.
* Dokumentation für Platzhalter korrigiert

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.
* Tabellenformat für SQL auf Azure-VM aktualisiert
* Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt
* „ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert

#### <a name="azrediscache"></a>Az.RedisCache
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.

#### <a name="azresources"></a>Az.Resources
* Dokumentation für Platzhalter korrigiert

#### <a name="azsql"></a>Az.Sql
* Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.
* Verbesserter Prozess für Klassifizierung mehrerer Spalten
* SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert
* Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss
* Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz
* Dokumentation für Platzhalter korrigiert

#### <a name="azwebsites"></a>Az.Websites
* „Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden
* Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.
* WebSites SDK aktualisiert
* AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt

## <a name="170---april-2019"></a>1.7.0: April 2019
### <a name="highlights-since-the-last-major-release"></a>Highlights seit der letzten Hauptversion
* Allgemeine Verfügbarkeit des `Az`-Moduls
* Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.
* Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.
* Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt
* Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt
* Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt
* Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration

#### <a name="azaccounts"></a>Az.Accounts
* „Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.
* „Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.

#### <a name="azautomation"></a>Az.Automation
* Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben. Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.
* Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung

#### <a name="azcompute"></a>Az.Compute
* Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt
* Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 3.0.2 aktualisiert
* Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert

#### <a name="azresources"></a>Az.Resources
* Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert
* Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert
    - Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856
* Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Unterstützung für Klassifizierung von Datenbankdaten

#### <a name="azstorage"></a>Az.Storage
* Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto
    - New-AzStorageContext
* Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0: März 2019
### <a name="highlights-since-the-last-major-release"></a>Highlights seit der letzten Hauptversion
* Allgemeine Verfügbarkeit des `Az`-Moduls
* Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.
* Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.
* Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt
* Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt
* Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt
* Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration

#### <a name="azautomation"></a>Az.Automation
* Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:
    * Dynamische Gruppierung
    * Pre-/Post-Skripts
    * Neustarteinstellung

#### <a name="azcompute"></a>Az.Compute
* Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben
* Computeclientbibliothek auf 25.0.0. aktualisiert

#### <a name="azkeyvault"></a>Az.KeyVault
* Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt

#### <a name="aznetwork"></a>Az.Network
* Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt
* Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen
* Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert
* Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden

#### <a name="azsql"></a>Az.Sql
* Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.

#### <a name="azstorage"></a>Az.Storage
* Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte

## <a name="150---march-2019"></a>1.5.0: März 2019
#### <a name="azaccounts"></a>Az.Accounts
* Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.
* Beispiele für „Connect-AzAccount“ wurden aktualisiert.

#### <a name="azautomation"></a>Az.Automation
* Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat
* „Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden. Jetzt werden alle Knoten zurückgegeben.

#### <a name="azcdn"></a>Az.Cdn
* Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen

#### <a name="azcompute"></a>Az.Compute
* Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 3.0.1 aktualisiert

#### <a name="azlogicapp"></a>Az.LogicApp
* „ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.

#### <a name="aznetwork"></a>Az.Network
* Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* SQL Server jetzt in Azure-VM-Support enthalten
* SDK-Update
* VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt
* „Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933
* Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240
* Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* „AuditingEndpointsCommunicator“ wird aktualisiert.
    - Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.

#### <a name="azstorage"></a>Az.Storage
* Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 – Februar 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Cmdlet „AddAzureASAccount“ als veraltet markiert

#### <a name="azautomation"></a>Az.Automation
* Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert
* Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt
* Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* „CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.

#### <a name="azcompute"></a>Az.Compute
* Problem mit ID-Parametersätzen behoben
* „Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist
* Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt
* „Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt

#### <a name="azeventhub"></a>Az.EventHub
* Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt

#### <a name="azkeyvault"></a>Az.KeyVault
* Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert

#### <a name="azlogicapp"></a>Az.LogicApp
* SKU „Basic“ für Integrationskonten hinzugefügt
* XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt
* Neue Cmdlets für Integrationskonto-Assemblys
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Neue Cmdlets für Integrationskonto-Batchkonfiguration
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Logik-App-SDK auf Version 4.1.0 aktualisiert

#### <a name="azmonitor"></a>Az.Monitor
* Hilfe für „Get-AzMetric“ aktualisiert

#### <a name="aznetwork"></a>Az.Network
* Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.
    - Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.
    - Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.

#### <a name="azresources"></a>Az.Resources
* Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166
* Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235
* Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219
* Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert

#### <a name="azsql"></a>Az.Sql
* Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt
* Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte

#### <a name="azwebsites"></a>Az.Websites
* Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert

## <a name="130---february-2019"></a>1.3.0: Februar 2019
#### <a name="azaccounts"></a>Az.Accounts
* Update auf die aktuelle Version von ClientRuntime durchgeführt

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul

#### <a name="azcompute"></a>Az.Compute
* AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt
* Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert
* Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.

#### <a name="azresources"></a>Az.Resources
* Kennzeichnung für Ressourcengruppen korrigiert
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166
* Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt
* Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt
* nullref-Ausnahme in Get-AzSqlCapability korrigiert

## <a name="121---january-2019"></a>1.2.1: Januar 2019
#### <a name="azaccounts"></a>Az.Accounts
* Release mit richtiger Version der Authentifizierung

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Release mit aktualisierter Authentifizierungsabhängigkeit

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Release mit aktualisierter Authentifizierungsabhängigkeit

## <a name="120---january-2019"></a>1.2.0: Januar 2019
#### <a name="azaccounts"></a>Az.Accounts
* Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt
* Fehlerhafte URLs für Onlinehilfe aktualisiert
* Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt

#### <a name="azaks"></a>Az.Aks
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azautomation"></a>Az.Automation
* Unterstützung für Python 2-Runbooks hinzugefügt
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azcdn"></a>Az.Cdn
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azcompute"></a>Az.Compute
* Cmdlet „Invoke-AzVMReimage“ hinzugefügt
* Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt
* Warnmeldung von „New-AzVM“ korrigiert

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azdatafactory"></a>Az.DataFactory
* Version des ADF .NET SDK auf 3.0.0 aktualisiert

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="aziothub"></a>Az.IotHub
* Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt

#### <a name="azkeyvault"></a>Az.KeyVault
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="aznetwork"></a>Az.Network
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azresources"></a>Az.Resources
* Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert
* Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden
* Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt
* Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747
* Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932
* Einige Fehlermeldungen wurden korrigiert.
* Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.
* Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.

#### <a name="azsignalr"></a>Az.SignalR
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azsql"></a>Az.Sql
* Fehlerhafte URLs für Onlinehilfe aktualisiert
* Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert
* Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat
* Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz

#### <a name="azstorage"></a>Az.Storage
* Fehlerhafte URLs für Onlinehilfe aktualisiert
* Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Fehlerhafte URLs für Onlinehilfe aktualisiert

#### <a name="azwebsites"></a>Az.Websites
* Fehlerhafte URLs für Onlinehilfe aktualisiert
* „New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.
* „New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.

## <a name="110---january-2019"></a>1.1.0 – Januar 2019
#### <a name="azaccounts"></a>Az.Accounts
* Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt

#### <a name="azcompute"></a>Az.Compute
* Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“
* Beschreibung der ID in Hilfedateien aktualisiert
* Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.
    - Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert

#### <a name="azeventgrid"></a>Az.EventGrid
* Zur Verwendung der API-Version 2019-01-01 aktualisiert
* Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01
    - New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:
        - Gültigkeitsdauer des Ereignisses
        - Maximale Anzahl von Übermittlungsversuchen für die Ereignisse
        - Endpunkt für unzustellbare Nachrichten
    - Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:
        - Gültigkeitsdauer des Ereignisses
        - Maximale Anzahl von Übermittlungsversuchen für die Ereignisse
        - Endpunkt für unzustellbare Nachrichten
* Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt
* Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat

#### <a name="aziothub"></a>Az.IotHub
* Auf die aktuelle Version des Iot Hub SDK aktualisiert

#### <a name="azlogicapp"></a>Az.LogicApp
* „Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf

#### <a name="azresources"></a>Az.Resources
* Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875
* Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert
* Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert
* Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“
    - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben

#### <a name="azsql"></a>Az.Sql
* Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert

#### <a name="azstorage"></a>Az.Storage
* Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird
    - New-AzStorageContext
* Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben
* Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben

## <a name="100---december-2018"></a>1.0.0 – Dezember 2018
### <a name="general"></a>Allgemein

- Allgemeine Verfügbarkeit des Az-Moduls
- Onlinehilfe für jedes Modul
- Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).
- Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azaccounts"></a>Az.Accounts
- Geändert von Az.Profile
- Feste Tabellenformate für Profil- und Kontexttypen

### <a name="azapimanagement"></a>Az.ApiManagement
- Korrekturen für #7002
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azbatch"></a>Az.Batch
- Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.
- Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azbilling"></a>Az.Billing
- Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azcognitivservices"></a>Az.CognitivServices
- Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt
- GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- ManagedIdentity-Unterstützung hinzugefügt

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azmonitor"></a>Az.Monitor
- Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azkeyvault"></a>Az.KeyVault
- Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt

### <a name="azmachinelearning"></a>Az.MachineLearning
- Cmdlets des Az.MachineLearningCompute-Moduls eingebunden

### <a name="azmedia"></a>Az.Media
- Veralteten -Tags-Alias aus New-AzMediaService entfernt

### <a name="aznetwork"></a>Az.Network
Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt
    - Neu hinzugefügte Cmdlets:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.
    - Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azprofile"></a>Az.Profile
- Modulnamen in Az.Accounts geändert

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azresources"></a>Az.Resources
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azservicefabric"></a>Az.ServiceFabric
- Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azsignalr"></a>Az.SIgnalR
- Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR

### <a name="azsql"></a>Az.Sql
- Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt
- Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azstorage"></a>Az.Storage
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

### <a name="azwebsites"></a>Az.Websites
- Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).

## <a name="070---december-2018"></a>0.7.0 – Dezember 2018

### <a name="general"></a>Allgemein

* Geringe Änderungen für anstehenden Übergang von AzureRM zu Az

### <a name="azcompute"></a>Az.Compute

* Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert

### <a name="azfrontdoor"></a>Az.FrontDoor

* Einige fehlerhafte Links behoben
    - In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.
    - Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.
* storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.

### <a name="azresources"></a>Az.Resources

* Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679
    - Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.

### <a name="azsql"></a>Az.Sql

* Geringe Änderungen für anstehenden Übergang von AzureRM zu Az
* Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben
* Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.

### <a name="azstorage"></a>Az.Storage

* -EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt
* Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird
    - Start-AzureStorageFileCopy
* Unterstützung der Konfiguration von statischen Websites
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp und Set-AzureRmWebAppSlot
    - Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen. Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.

## <a name="061---november-2018"></a>0.6.1 – November 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

### <a name="azautomation"></a>Az.Automation
* Swagger-basierte Azure Automation-Cmdlets
* Cmdlets zur Updateverwaltung hinzugefügt
* Cmdlets zur Quellcodeverwaltung hinzugefügt
* Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt
* DSC-Befehl für die Knotenregistrierung korrigiert

### <a name="azcompute"></a>Az.Compute
* Identitätsproblem für SystemAssigned-Identität korrigiert
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert

### <a name="aznetwork"></a>Az.Network
* Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError
* ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt
* Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt
* Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben
* Richtlinienzeitzone in Großschreibung geändert

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“
* Abhängigkeiten für Typzuordnungsproblem aktualisiert

### <a name="azrelay"></a>Az.Relay
* Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht

### <a name="azresources"></a>Az.Resources
* Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert
* Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt
* Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt

### <a name="azsql"></a>Az.Sql
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

## <a name="050---november-2018"></a>0.5.0 – November 2018
#### <a name="general"></a>Allgemein
* Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)

#### <a name="azprofile"></a>Az.Profile
* Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird
* Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt
* Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert
* Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert
    - https://github.com/Azure/azure-powershell/issues/6936
* Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben
    - https://github.com/Azure/azure-powershell/issues/7453
* Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben
    - https://github.com/Azure/azure-powershell/issues/7462
* Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt

#### <a name="azcompute"></a>Az.Compute
* Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt
* „Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an
* Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aktualisierung des DataLake-Pakets auf 1.1.10
* Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt

#### <a name="azinsights"></a>Az.Insights
* Problem Nr. 7267 behoben (Bereich für automatische Skalierung)
    - Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)
* Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.
    - Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.

#### <a name="aznetwork"></a>Az.Network
* „PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Cmdlets für Richtlinienwartung hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402
    - Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“

#### <a name="azservicebus"></a>Az.ServiceBus
* Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Hinzufügen des Zertifikats zu Linux VMSS korrigiert
* „Add-AzServiceFabricClusterCertificate“ korrigiert
    - Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)
    - Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)
* „Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird

## <a name="040---october-2018"></a>0.4.0 – Oktober 2018
#### <a name="azprofile"></a>Az.Profile
* Problem mit „Get-AzSubscription“ in Cloud Shell behoben
* Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird

#### <a name="azcompute"></a>Az.Compute
* Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird
* ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Unterstützung für VNET-Regeln hinzugefügt
    - Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.
    - Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.
    - Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.

#### <a name="aznetwork"></a>Az.Network
* Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.
* ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.

#### <a name="azresources"></a>Az.Resources
* Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde. Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.

## <a name="030---october-2018"></a>0.3.0 – Oktober 2018
#### <a name="azurestorage"></a>Azure.Storage
* Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.
    - Get-AzStorageUsage

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* „Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.

#### <a name="azcompute"></a>Az.Compute
* Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden
* Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.
* Tippfehler in der Azure Disk Encryption-Statusmeldung behoben

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.

#### <a name="aznetwork"></a>Az.Network
* NetworkProfile-Funktionalität wurde hinzugefügt. Neue Cmdlets hinzugefügt
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Dienstzuordnungslink in Subnetzmodell hinzugefügt
* Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt
* Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt

#### <a name="azrediscache"></a>Az.RedisCache
* Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig. P5 in Popup „PSArgumentCompleter“ hinzugefügt

#### <a name="azresources"></a>Az.Resources
* Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt
* Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält

#### <a name="azsql"></a>Az.Sql
* Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben

#### <a name="azwebsites"></a>Az.Websites
* Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container
* Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App

## <a name="020---september-2018"></a>0.2.0 – September 2018
 Erstrelease
