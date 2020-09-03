---
title: Azure PowerShell-Änderungsprotokoll | Microsoft-Dokumentation
description: Hierbei handelt es sich um einen Verlauf der Änderungen, die in der neuesten Version an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: fca8b618a2b04d10df51a34942125435a403ca56
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243904"
---
# <a name="release-notes"></a>Versionshinweise

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Hierbei handelt es sich um eine Liste der Änderungen, die in dieser Version an Azure PowerShell vorgenommen wurden.

## <a name="20170925---version-440"></a>25.09.2017 – Version 4.4.0
* AnalysisServices
  * Neues Datenebenen-Cmdlet hinzugefügt, um die Synchronisierung von Datenbanken aus Instanzen mit Lese-/Schreibzugriff mit schreibgeschützten Instanzen zu ermöglichen
    - Hilfedatei für das Cmdlet hinzugefügt
    - In-Memory-Tests und Szenariotest hinzugefügt (nur live)
  * Fehler im Cmdlet „Add-AzureAsAccount“ korrigiert
* Automation
  * Hilfedokumente für Cmdlets korrigiert, die in der vorherigen Version korrigiert wurden
  * Vier neue Cmdlets zur Unterstützung des gestaffelten Rollouts von DSC-Knotenkonfigurationen hinzugefügt
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Integration in Cognitive Services Management SDK (Version 2.0.0).
  * „Get-AzureRmCognitiveServicesAccount“ verfügt jetzt über ordnungsgemäße Paginierungsunterstützung.
* Compute
  * Befehlsausführungsfeature:
    - Neues Cmdlet: „Invoke-AzureRmVMRunCommand“ ruft einen Ausführungsbefehl auf einem virtuellen Computer auf.
    - Neues Cmdlet: „Get-AzureRmVMRunCommandDocument“ zeigt verfügbare Ausführungsbefehlsdokumente an.
  * Parameter „StorageAccountType“ zu „Set-AzureRmDataDisk“ hinzugefügt
  * Verfügbarkeitszonenunterstützung für virtuellen Computer, VM-Skalierungsgruppe und Datenträger
    - Neuer Parameter: „Zone“ wurde zu „New-AzureRmVM“, „New-AzureRmVMConfig“, „New-AzureRmVmssConfig“ und „New-AzureRmDiskConfig“ hinzugefügt.
  * Feature für paralleles Upgraden von VM-Skalierungsgruppen:
    - Neues Cmdlet: „Start-AzureRmVmssRollingOSUpgrade“ ruft das parallele Betriebssystemupgrade für die VM-Skalierungsgruppe auf.
    - Neues Cmdlet: „Set-AzureRmVmssRollingUpgradePolicy“ legt die Upgraderichtlinie für das parallele Upgrade der VM-Skalierungsgruppe fest.
    - Neues Cmdlet: „Stop-AzureRmVmssRollingUpgrade“ bricht das parallele Betriebssystemupgrade für die VM-Skalierungsgruppe ab.
    - Neues Cmdlet: „Get-AzureRmVmssRollingUpgrade“ zeigt den Status des parallelen Upgrades der VM-Skalierungsgruppe an.
  * AssignIdentity-Wechselparameter für vom System zugewiesene Identität eingeführt.
    - Neuer Parameter: „AssignIdentity“ wurde zu „New-AzureRmVMConfig“, „New-AzureRmVmssConfig“ und „Update-AzureRmVM“ hinzugefügt.
  * VMSS-Datenträgerverschlüsselungsfeature:
    - Neues Cmdlet: „Set-AzureRmVmssDiskEncryptionExtension“ aktiviert die Datenträgerverschlüsselung in der VM-Skalierungsgruppe.
    - Neues Cmdlet: „Disable-AzureRmVmssDiskEncryption“ deaktiviert die Datenträgerverschlüsselung in der VM-Skalierungsgruppe.
    - Neues Cmdlet: „Get-AzureRmVmssDiskEncryptionStatus“ zeigt den Status der Datenträgerverschlüsselung einer VM-Skalierungsgruppe an.
    - Neues Cmdlet: „Get-AzureRmVmssVMDiskEncryptionStatus“ zeigt den Status der Datenträgerverschlüsselung virtueller Computer in einer VM-Skalierungsgruppe an.
* ContainerInstance
  * PowerShell-Cmdlets für Azure-Containerinstanz hinzugefügt
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Einblicke
  * Neues Cmdlet: Disable-AzureRmActivityLogAlert
    - Ein neues Cmdlet zum Deaktivieren einer vorhandenen Aktivitätsprotokollwarnung.
    - Optional können mit diesem Cmdlet auch die Tags festgelegt werden.
  * Neues Cmdlet: Enable-AzureRmActivityLogAlert
    - Ein neues Cmdlet zum Aktivieren einer vorhandenen Aktivitätsprotokollwarnung.
    - Optional können mit diesem Cmdlet auch die Tags festgelegt werden.
  * Neues Cmdlet: Get-AzureRmActivityLogAlert
    - Ein neues Cmdlet zum Abrufen einzelner oder mehrerer Aktivitätsprotokollwarnungen.
    - Die Warnungen können nach Name, Ressourcengruppe oder Abonnement abgerufen werden.
  * Neues Cmdlet: New-AzureRmActionGroup
    - Ein neues Cmdlet zum Erstellen eines ActionGroup-Objekts im Arbeitsspeicher (ohne Anforderung).
  * Neues Cmdlet: New-AzureRmActivityLogAlertCondition
    - Ein neues Cmdlet zum Erstellen eines Blattbedingungsobjekts für Aktivitätsprotokollwarnungen im Arbeitsspeicher (ohne Anforderung).
  * Neues Cmdlet: Set-AzureRmActivityLogAlert
    - Ein neues Cmdlet zum Erstellen oder Aktualisieren einer Aktivitätsprotokollwarnung.
  * Neues Cmdlet: Remove-AzureRmActivityLogAlert
    - Ein neues Cmdlet zum Entfernen einer Aktivitätsprotokollwarnung.
  * Neues Cmdlet: Set-AzureRmActionGroup
    - Ein neues Cmdlet zum Erstellen einer neuen Aktionsgruppe oder zum Aktualisieren einer vorhandenen Aktivitätsgruppe.
  * Neues Cmdlet: Get-AzureRmActionGroup
    - Ein neues Cmdlet zum Abrufen einzelner oder mehrerer Aktionsgruppen.
    - Die Aktionsgruppen können nach Name, Ressourcengruppe oder Abonnement abgerufen werden.
  * Neues Cmdlet: Remove-AzureRmActionGroup
    - Ein neues Cmdlet zum Entfernen einer Aktionsgruppe.
  * Neues Cmdlet: New-AzureRmActionGroupReceiver
    - Ein neues Cmdlet zum Erstellen eines neuen Aktionsgruppenempfängers im Arbeitsspeicher.
* KeyVault
  * Neue/aktualisierte Cmdlets zur Unterstützung von vorläufigem Löschen für KeyVault-Zertifikate
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Netzwerk
  * Unterstützung für Endpunktdienste zu Subnetzen in virtuellen Netzwerken hinzugefügt
    - „Add-AzureRmVirtualSubnetConfig“ aktualisiert: Zusätzlicher optionaler Parameter: -ServiceEndpoint
    - „New-AzureRmVirtualSubnetConfig“ aktualisiert: Zusätzlicher optionaler Parameter: -ServiceEndpoint
    - „Set-AzureRmVirtualSubnetConfig“ aktualisiert: Zusätzlicher optionaler Parameter: -ServiceEndpoint
  * Cmdlet zum Auflisten der am Standort verfügbaren Endpunktdienste hinzugefügt
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Möglichkeit zum Konfigurieren der externen Radius-basierten P2S-Authentifizierung zu folgenden Cmdlets hinzugefügt:
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Cmdlet zum Generieren von VPN-Profilen für externe Radius-basierte P2S-Authentifizierung
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Unterstützung für SKU-Parameter zu öffentlichen IP-Adressen und Lastenausgleichsmodulen hinzugefügt
    - „New-AzureRMLoadBalancer“ aktualisiert: Optionaler Parameter hinzugefügt: -Sku
    - „New-AzureRMPublicIpAddress“ aktualisiert: Optionaler Parameter hinzugefügt: -Sku
  * Unterstützung für „DisableOutboundSNAT“ zu Lastenausgleichsregeln hinzugefügt
    - „New-AzureRMLoadBalancerRuleConfig“ aktualisiert: Optionaler Parameter hinzugefügt: DisableOutboundSNAT
    - „Add-AzureRMLoadBalancerRuleConfig“ aktualisiert: Optionaler Parameter hinzugefügt: DisableOutboundSNAT
    - „Set-AzureRMLoadBalancerRuleConfig“ aktualisiert: Optionaler Parameter hinzugefügt: DisableOutboundSNAT
  * Unterstützung für IkeV2-P2S hinzugefügt
    - „New-AzureRmVirtualNetworkGateway“ aktualisiert: Optionaler Parameter hinzugefügt: -VpnClientProtocol. Standardwert: [ "SSTP", "IkeV2" ]
    - „Set-AzureRmVirtualNetworkGateway“ aktualisiert: Optionaler Parameter hinzugefügt: -VpnClientProtocol
  * Unterstützung für MultiValued-Regeln in Netzwerksicherheitsregeln und effektiven Netzwerksicherheitsregeln hinzugefügt
    - „Add-AzureRmNetworkSecurityRuleConfig“ hinzugefügt: Parameter „SourcePortRange“, „DestinationPortRange“ und „SourceAddressPrefix“ aktualisiert, sodass sie eine Liste mit Zeichenfolgen akzeptieren
    - „New-AzureRmNetworkSecurityRuleConfig“ aktualisiert: Parameter „SourcePortRange“, „DestinationPortRange“ und „SourceAddressPrefix“ aktualisiert, sodass sie eine Liste mit Zeichenfolgen akzeptieren
    - „Set-AzureRmNetworkSecurityRuleConfig“ aktualisiert: Parameter „SourcePortRange“, „DestinationPortRange“ und „SourceAddressPrefix“ aktualisiert, sodass sie eine Liste mit Zeichenfolgen akzeptieren
    - „Add-AzureRmNetworkSecurityRuleConfig“ hinzugefügt: Parameter „SourcePortRange“, „DestinationPortRange“ und „SourceAddressPrefix“ aktualisiert, sodass sie eine Liste mit Zeichenfolgen akzeptieren
    - „New-AzureRmNetworkSecurityGroup“ aktualisiert: SecurityRules-Parameter aktualisiert, sodass er die Parameter „SourcePortRange“, „DestinationPortRange“ und „SourceAddressPrefix“ akzeptiert, bei denen es sich um eine Liste mit Zeichenfolgen im PSSecurityRule-Objekt handelt
    - „Get-AzureRmEffectiveNetworkSecurityGroup“ aktualisiert: Parameter „TagMap“ hinzugefügt
    - „Get-AzureRmEffectiveNetworkSecurityGroup“ aktualisiert: Zurückgegebenes PSEffectiveSecurityRule-Objekt mit den Parametern „SourcePortRange“, „DestinationPortRange“ und „SourceAddressPrefix“ aktualisiert, bei denen es sich um eine Liste mit Zeichenfolgen handelt
  * Unterstützung für DDoS-Schutz für virtuelle Netzwerke hinzugefügt
    - „New-AzureRmVirtualNetwork“ aktualisiert: Switch-Parameter „EnableDDoSProtection“ und „EnableVmProtection“ hinzugefügt
    - Eigenschaften „EnableDDoSProtection“ und „EnableVmProtection“ im PSVirtualNetwork-Objekt hinzugefügt
  * Unterstützung für hoch verfügbaren internen Lastenausgleich hinzugefügt
    - „Add-AzureRmLoadBalancerRuleConfig“ aktualisiert: „All“ als zulässiger Wert für Parameter „Protocol“ hinzugefügt
    - „New-AzureRmLoadBalancerRuleConfig“ aktualisiert: „All“ als zulässiger Wert für Parameter „Protocol“ hinzugefügt
    - „Set-AzureRmLoadBalancerRuleConfig“ aktualisiert: „All“ als zulässiger Wert für Parameter „Protocol“ hinzugefügt
  * Unterstützung für Anwendungssicherheitsgruppen hinzugefügt
    - „New-AzureRmApplicationSecurityGroup“ hinzugefügt
    - „Get-AzureRmApplicationSecurityGroup“ hinzugefügt
    - „Remove-AzureRmApplicationSecurityGroup“ hinzugefügt
    - „New-AzureRmNetworkInterface“ aktualisiert: Optionale Parameter „ApplicationSecurityGroup“ und „ApplicationSecurityGroupId“ hinzugefügt
    - „New-AzureRmNetworkInterfaceIpConfig“ aktualisiert: Optionale Parameter „ApplicationSecurityGroup“ und „ApplicationSecurityGroupId“ hinzugefügt
    - „Add-AzureRmNetworkInterfaceIpConfig“ aktualisiert: Optionale Parameter „ApplicationSecurityGroup“ und „ApplicationSecurityGroupId“ hinzugefügt
    - „Set-AzureRmNetworkInterfaceIpConfig“ aktualisiert: Optionale Parameter „ApplicationSecurityGroup“ und „ApplicationSecurityGroupId“ hinzugefügt
    - „New-AzureRmNetworkSecurityRuleConfig“ aktualisiert: Optionale Parameter „SourceApplicationSecurityGroup“, „SourceApplicationSecurityGroupId“, „DestinationApplicationSecurityGroup“ und „DestinationApplicationSecurityGroupId“ hinzugefügt
    - „Add-AzureRmNetworkSecurityRuleConfig“ hinzugefügt: Optionale Parameter „SourceApplicationSecurityGroup“, „SourceApplicationSecurityGroupId“, „DestinationApplicationSecurityGroup“ und „DestinationApplicationSecurityGroupId“ hinzugefügt
    - „Set-AzureRmNetworkSecurityRuleConfig“ aktualisiert: Optionale Parameter „SourceApplicationSecurityGroup“, „SourceApplicationSecurityGroupId“, „DestinationApplicationSecurityGroup“ und „DestinationApplicationSecurityGroupId“ hinzugefügt
  * Neue Befehle für VpnDeviceConfiguration-Skripts hinzugefügt
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profil
  * Start-Job-Unterstützung für AzureRm-Cmdlets.
    * Parameter „-AzureRmContext“ für alle AzureRm-Cmdlets hinzugefügt. Der Parameter kann einen Kontext (Ausgabe eines Context-Cmdlets) akzeptieren.
      - Allgemeines Muster für Aufträge mit DEAKTIVIERTER Kontextpersistenz: `Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Allgemeines Muster für Aufträge mit AKTIVIERTER Kontextpersistenz: `Start-Job {New-AzureRmVM [... other parameters]}`
  * Sitzungsübergreifendes Speichern von Anmeldeinformationen – neue Cmdlets:
    - Enable-AzureRmContextAutosave: Dient zum Aktivieren der sitzungsübergreifenden Persistenz von Anmeldeinformationen.
    - Disable-AzureRmContextAutosave: Dient zum Deaktivieren der sitzungsübergreifenden Persistenz von Anmeldeinformationen.
  * Verwalten von Kontextinformationen – neue Cmdlets
    - Select-AzureRmContext: Dient zum Auswählen des aktiven benannten Kontexts.
    - Rename-AzureRmContext: Dient zum Umbenennen eines vorhandenen Kontexts, um leichter darauf verweisen zu können.
    - Remove-AzureRmContext: Dient zum Entfernen eines vorhandenen Kontexts.
    - Remove-AzureRmAccount: Dient zum Entfernen aller einem Konto zugeordneten Anmeldeinformationen, Abonnements und Mandanten.
  * Verwalten von Kontextinformationen – Cmdlet-Änderungen
    - „Scope = (Process | CurrentUser)“ für alle Cmdlets hinzugefügt, die Anmeldeinformationen ändern
    - Get-AzureRmContext: ListAvailable-Parameter zum Auflisten aller gespeicherten Kontexte hinzugefügt
* Ressourcen
  * PolicySetDefinition-Cmdlets hinzugefügt
    - Cmdlet „New-AzureRmPolicySetDefinition“ zum Erstellen einer Richtliniensatzdefinition
    - Cmdlet „Get-AzureRmPolicySetDefinition“ zum Auflisten aller Richtliniensatzdefinitionen oder zum Abrufen einer bestimmten Richtliniensatzdefinition
    - Cmdlet „Remove-AzureRmPolicySetDefinition“ zum Löschen einer Richtliniensatzdefinition
    - Cmdlet „Set-AzureRmPolicySetDefinition“ zum Aktualisieren einer vorhandenen Richtliniensatzdefinition
  * Parameter „Add -PolicySetDefinition“, „-Sku“ und „-NotScope“ zu den Cmdlets „New-AzureRmPolicyAssignment“ und „Set-AzureRmPolicyAssignment“ hinzugefügt
  * Unterstützung der Übergabe der Richtlinien-URL an die Cmdlets „New-AzureRmPolicyDefinition“ und „Set-AzureRmPolicyDefinition“ hinzugefügt
  * Parameter „-Mode“ zum Cmdlet „New-AzureRmPolicyDefinition“ hinzugefügt
  * Unterstützung des Entfernens der Rollenzuweisung mithilfe des PSRoleAssignment-Objekts hinzugefügt
    - Benutzer können jetzt „PSRoleassignmnet inputobject“ mit dem Cmdlet „Remove-AzureRMRoleAssignment“ verwenden, um die Rollenzuweisung zu entfernen.
  * ManagedApplication-Cmdlets hinzugefügt
    - Cmdlet „New-AzureRmManagedApplication“ zum Erstellen einer verwalteten Anwendung
    - Cmdlet „Get-AzureRmManagedApplication“ zum Auflisten aller verwalteten Anwendungen unter einem Abonnement oder zum Abrufen einer bestimmten verwalteten Anwendung
    - Cmdlet „Remove-AzureRmManagedApplication“ zum Löschen einer verwalteten Anwendung
    - Cmdlet „Set-AzureRmManagedApplication“ zum Aktualisieren einer vorhandenen verwalteten Anwendung
  * ManagedApplicationDefinition-Cmdlets hinzugefügt
    - Cmdlet „New-AzureRmManagedApplicationDefinition“ zum Erstellen einer Definition für verwaltete Anwendungen unter Verwendung eines ZIP-Datei-URI oder unter Verwendung der JSON-Dateien „mainTemplate“ und „createUiDefinition“
    - Cmdlet „Get-AzureRmManagedApplicationDefinition“ zum Auflisten aller Definitionen für verwaltete Anwendungen unter einer Ressourcengruppe oder zum Abrufen einer bestimmten Definition für verwaltete Anwendungen
    - Cmdlet „Remove-AzureRmManagedApplicationDefinition“ zum Löschen einer Definition für verwaltete Anwendungen
    - Cmdlet „Set-AzureRmManagedApplicationDefinition“ zum Aktualisieren einer vorhandenen Definition für verwaltete Anwendungen
* Sql
  * Unterstützung für VNET-Regeln hinzugefügt
    - Cmdlet „Get-AzureRmSqlServerVirtualNetworkRule“ zum Abrufen der VNET-Regeln anhand eines spezifischen Regelnamens oder zum Auflisten einer Liste mit VNET-Regeln einer Azure SQL Server-Instanz hinzugefügt
    - Cmdlet „Set-AzureRmSqlServerVirtualNetworkRule“ zum Ändern des virtuellen Netzwerks hinzugefügt, auf das die Regel verweist
    - Cmdlet „Remove-AzureRmSqlServerVirtualNetworkRule“ zum Entfernen einer VNET-Regel für eine Azure SQL Server-Instanz hinzugefügt
    - Cmdlet „New-AzureRmSqlServerVirtualNetworkRule“ zum Erstellen einer neuen VNET-Regel für eine Azure SQL Server-Instanz hinzugefügt
* Websites
  * PremiumV2-Tarif für App Service-Pläne hinzugefügt
* Azure.Storage
  * Upgrade auf Azure Storage-Clientbibliothek 8.4.0 und Azure Storage DataMovement-Bibliothek 0.6.1 durchgeführt
  * PremiumPageBlobTier-Unterstützung in Upload- und Copy Blob-API hinzugefügt
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Konsolenausgabeformat von „AzureStorageContainer“, „AzureStorageBlob“, „AzureStorageQueue“ und „AzureStorageTable“ optimiert
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 – Version 4.3.1
  * Update zur Behebung des Problems beim Signieren von Assemblys

## <a name="20170807---version-430"></a>2017.08.07 – Version 4.3.0
* AnalysisServices
  * Fehler in „Set-AzureRmAnalysisServciesServer“ behoben
    - Wenn kein Administrator angegeben wurde, wird der Administrator entfernt.
  * „BackupBlobContainerUri“ zu „New-AzureRmAnalysisServicesServer“ und „Set-AzureRmAnalysisServicesServer“ hinzugefügt
    - Diese Option muss zum Festlegen bzw. Deaktivieren des Sicherungsblobcontainers für die Sicherung bzw. Wiederherstellung des Azure Analysis Services-Servers aktiviert werden.
  * SKU-Suche in „New-AzureRmAnalysisServicesServer“ und „Set-AzureRmAnalysisServicesServer“ aktualisiert
    - Die hartcodierte SKU in der dynamischen Suche wurde geändert.
  * „Add-AzureAnalysisServicesAccount“ zur Unterstützung der Anmeldung mit einem Dienstprinzipal
* Automation
  * Änderungen an AutomationDSC*-Cmdlets, damit mehr als 100 Datensätze abgerufen werden können
  * Das Problem, bei dem nach dem Aufrufen einiger Automation-Cmdlets (z.B. „Get-AzureRmAutomationVariable“, „Get-AzureRmAutomationJob“) die Verbose-Streams nicht mehr funktionieren, wurde behoben.
  * Unterstützung zur Verwaltung des Knotenkonfigurationsbuilds in „StartAzureAutomationDscCompilationJob“ und „ImportAzureAutomationDscNodeConfiguration“ hinzugefügt
  * Fehlerbehebungen für vorhandene Probleme – Korrektur des Problems mit Alias #3775 und runOn-Alias, Unterstützung für Hybrid Worker.
* Compute
  * Set-AzureRmVMAEMExtension: Unterstützung für neue Premium-Datenträgergrößen hinzugefügt
  * Set-AzureRmVMAEMExtension: Unterstützung für M-Serie hinzugefügt
  * ForceUpdateTag-Parameter zu „Add-AzureRmVmssExtension“ hinzugefügt
  * Primary-Parameter zu „New-AzureRmVmssIpConfig“ hinzugefügt
  * „EnableAcceleratedNetworking-Parameter“ zu „Add-AzureRmVmssNetworkInterfaceConfig“ hinzugefügt
  * „InstanceId“ zu „Set-AzureRmVmss“ hinzugefügt
  * „MaintenanceRedeployStatus“ für die Ausgabe von „Get-AzureRmVM -Status“ verfügbar gemacht
  * Einschränkungen und Funktionen für das Tabellenformat von „Get-AzureRmComputeResourceSku“ verfügbar gemacht
* DataLakeStore
  * Behebung des Problems: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * ResourceGroup-Eigenschaft zu „NamespaceAttributes“ hinzugefügt
    - „ResourceGroup“ ruft den Namen der Ressourcengruppe ab, in der sich der Namespace befindet.
  * Cmdlets mit Parametersätzen für „NameSpace“ und „EventHub“ für AuthorizationRule aktualisiert
    - New-AzureRmEventHubAuthorizationRule: Fügt dem vorhandenen Attribut „NameSpace“ oder „EventHub“ eine AuthorizationRule hinzu.
    - Get-AzureRmEventHubAuthorizationRule: Ruft die AuthorizationRule bzw. eine Liste von AuthorizationRules für das vorhandene Attribut „NameSpace“ oder „EventHub“ ab.
    - Set-AzureRmEventHubAuthorizationRule: Aktualisiert die Eigenschaften einer vorhandenen AuthorizationRule der Attribute „EventHub“ und „NameSpace“.
    - Remove-AzureRmEventHubAuthorizationRule: Löscht die vorhandene AuthorizationRule des vorhandenen Attributs „NameSpace“ oder „EventHub“.
    - New-AzureRmEventHubKey: Generiert einen neuen primären/sekundären Schlüssel für die AuthorizationRule des vorhandenen Attributs „NameSpace“ oder „EventHub“.
    - Get-AzureRmEventHubKey: Ruft einen primären/sekundären Schlüssel für die AuthorizationRule des vorhandenen Attributs „NameSpace“ oder „EventHub“ ab.
* Netzwerk
    * Unterstützung für IPv6 und neuer optionale Parameter „-PeerAddressType“
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: IPv6-Unterstützung hinzugefügt. Neuer optionaler Parameter hinzugefügt
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: IPv6-Unterstützung hinzugefügt. Neuer optionaler Parameter hinzugefügt
    * Parameter „-ProbeEnabled“ als veraltet markiert
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * Die Datensammlung wurde standardmäßig aktiviert. Zur Verbesserung der Benutzerfreundlichkeit werden Nutzungsdaten von Microsoft gesammelt. Die Daten sind anonymisiert und enthalten keine Befehlszeilenargument-Werte.
      - Verwenden Sie das Cmdlet „Disable-AzureRmDataCollection“, um die Funktion zu deaktivieren.
      - Verwenden Sie das Cmdlet „Enable-AzureRmDataCollection“, um diese Funktion zu aktivieren.
* Ressourcen
    * Unterstützung zum Überprüfen von Bereichen für die folgenden roledefinition- und roleassignment-Cmdlets vor dem Senden der Anforderung an ARM hinzugefügt
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * Es wurden die folgenden neuen Cmdlets für AuthorizationRules für „NameSpace“, „Queue“ und „Topic“ hinzugefügt. Die Autorisierungsregelvorgänge werden gemäß dem Parametersatz ausgeführt.
    - New-AzureRmServiceBusAuthorizationRule: Fügt eine neue AuthorizationRule zum vorhandenen ServiceBus-Attribut „NameSpace“, „Queue“ oder „Topic“ hinzu.
    - Get-AzureRmServiceBusAuthorizationRule: Ruft die AuthorizationRule bzw. eine Liste von AuthorizationRules für das vorhandene ServiceBus-Attribut „NameSpace“, „Queue“ oder „Topic“ ab.
    - Set-AzureRmServiceBusAuthorizationRule: Aktualisiert die Eigenschaften einer vorhandenen AuthorizationRule der ServiceBus-Attribute „NameSpace“, „Queue“ oder „Topic“.
    - New-AzureRmServiceBusKey: Generiert einen neuen primären/sekundären Schlüssel für die AuthorizationRule des vorhandenen ServiceBus-Attributs „NameSpace“, „Queue“ oder „Topic“.
    - Get-AzureRmServiceBusKey: Ruft den primären/sekundären Schlüssel für die AuthorizationRule des vorhandenen ServiceBus-Attributs „NameSpace“, „Queue“ oder „Topic“ ab.
    - Remove-AzureRmServiceBusNamespaceAuthorizationRule: Löscht die vorhandene AuthorizationRule des ServiceBus-Attributs „NameSpace“, „Queue“ oder „Topic“.
  * ResourceGroup-Eigenschaft zu „NamespaceAttributes“ hinzugefügt

* Sql
    * „Set-AzureRmSqlServerTransparentDataEncryptionProtector“ aktualisiert, um Warnung anzuzeigen und die Bestätigung anzufordern, ob der Verschlüsselungsschutztyp auf „AzureKeyVault“ festgelegt werden soll
    * Neue aktualisierte Cmdlets für Überwachungseinstellungen hinzugefügt
      - Das Cmdlet „Get-AzureRmSqlDatabaseAuditing“ ruft Überwachungseinstellungen einer Azure SQL-Datenbank ab.
      - Das Cmdlet „Get-AzureRmSqlServerAuditing“ ruft Überwachungseinstellungen eines Azure SQL-Servers ab.
      - Das Cmdlet „Set-AzureRmSqlDatabaseAuditing“ ändert die Überwachungseinstellungen einer Azure SQL-Datenbank.
      - Das Cmdlet „Set-AzureRmSqlServerAuditing“ ändert die Überwachungseinstellungen eines Azure SQL-Servers.
    * Vorhandene Cmdlets für die Überwachungsrichtlinie als veraltet markiert
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Bei der Analyse von Schemadateien für „Update-AzureRmSqlSyncGroup“ gilt nun die Groß-/Kleinschreibung.
* Storage
    * Unterstützung für „NeworkRule“ zu Cmdlets für Speicherkonten mit Ressourcenmodus hinzugefügt
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17 – Version 4.2.1
* Compute
  - Problem mit den Cmdlets zum Erstellen und Aktualisieren von VM-Datenträgern und VM-Datenträgermomentaufnahmen behoben, Link: [<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* Profil
  - Problem mit der nicht interaktiven Benutzerauthentifizierung in RDFE behoben, Link: [<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - Problem mit der nicht interaktiven Benutzerauthentifizierung behoben, Link :[<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.7.11 – Version 4.2.0
* AnalysisServices
    * Neue API für die Datenebene hinzugefügt
        - Einführung einer API zum Abrufen des AS-Serverprotokolls, „Export-AzureAnalysisServicesInstanceLog“
* Automation
    * Ordnungsgemäße Einstellung des TimeZone-Werts für wöchentliche und monatliche Zeitpläne für „New-AzureRmAutomationSchedule“
        - Weitere Informationen finden Sie unter diesem Problem: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Neues Cmdlet „Get-AzureBatchJobPreparationAndReleaseTaskStatus“ hinzugefügt.
    - Start und Ende für den Bytebereich zu Get-AzureBatchNodeFileContent-Parametern hinzugefügt.
* CognitiveServices
    * Integration in Cognitive Services Management SDK, Version 1.0.0.
    * Fehler bei der Längenüberprüfung für Kontonamen behoben.
* Compute
    * Speicherkontotyp-Unterstützung für Imagedatenträger:
        - StorageAccountType-Parameter zu „Set-AzureRmImageOsDisk“ und „Add-AzureRmImageDataDisk“ hinzugefügt
    * PrivateIP- und PublicIP-Feature in VMSS-IP-Konfiguration:
        - Folgende Namen wurden zu „New-AzureRmVmssIpConfig“ hinzugefügt: PrivateIPAddressVersion, PublicIPAddressConfigurationName, PublicIPAddressConfigurationIdleTimeoutInMinutes, DnsSetting
        - PrivateIPAddressVersion-Parameter zum Angeben von IPv4 oder IPv6 zu „New-AzureRmVmssIpConfig“ hinzugefügt
    * Feature für die Leistungsverwaltung:
        - PerformMaintenance-Parameter zu „Restart-AzureRmVM“ hinzugefügt.
        - „Get-AzureRmVM -Status“ zeigt Informationen zur Leistungsverwaltung der jeweiligen VM an
    * Feature für die Identität des virtuellen Computers:
        - IdentityType-Parameter zu „New-AzureRmVMConfig“ und „UpdateAzureRmVM“ hinzugefügt
        - „Get-AzureRmVM“ zeigt die Informationen zur Identität der jeweiligen VM an
    * Feature für die VMSS-Identität:
        - IdentityType-Parameter zu „New-AzureRmVmssConfig“ hinzugefügt
        - „Get-AzureRmVmss“ zeigt die Informationen zur Identität der jeweiligen VMSS an
    * Feature für die VMSS-Startdiagnose:
        - Neues Cmdlet zum Festlegen der Startdiagnose für das VMSS-Objekt: Set-AzureRmVmssBootDiagnostics
        - BootDiagnostic-Parameter zu „New-AzureRmVmssConfig“ hinzugefügt
    * VMSS-LicenseType-Feature:
        - LicenseType-Parameter zu „New-AzureRmVmssConfig“ hinzugefügt
    * RecoveryPolicyMode-Unterstützung:
        - RecoveryPolicyMode-Parameter zu „New-AzureRmVmssConfig“ hinzugefügt
    * Feature für Computeressourcen-SKU:
        - Neues Cmdlet „Get-AzureRmComputeResourceSku“ listet alle Computeressourcen-SKUs auf
* DataFactories
    * „New-AzureRmDataFactoryGatewayKey“ eingestellt
    * Einführung eines Schlüsselfeatures für die Gatewayauthentifizierung durch Hinzufügen von „New-AzureRmDataFactoryGatewayAuthKey“ und „Get-AzureRmDataFactoryGatewayAuthKey“
* DataLakeAnalytics
    * Unterstützung für Computerichtlinie CRUD über die folgenden Befehle hinzugefügt:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Es wurde Unterstützung für Auftragsbeziehungs-Metadaten als Hilfe bei wiederkehrenden Aufträgen und Auftragspipelines hinzugefügt. Folgende Befehle wurden aktualisiert oder hinzugefügt:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * Die Tokenzielgruppe für die Auftrags- und die Katalog-API wurde auf die Verwendung des richtigen, Data Lake-spezifischen Zielpublikums anstelle des Azure-Ressourcenzielpublikums aktualisiert.
* DataLakeStore
    * Unterstützung für die benutzerverwaltete KeyVault-Schlüsselrotation im Cmdlet „Set-AzureRMDataLakeStoreAccount“ hinzugefügt
    * Quality of Life-Update hinzugefügt, um automatisch einen `enableKeyVault`-Aufruf auszulösen, wenn ein benutzerverwalteter KeyVault hinzugefügt oder ein Schlüssel rotiert wird.
    * Die Tokenzielgruppe für die Auftrags- und die Katalog-API wurde auf die Verwendung des richtigen, Data Lake-spezifischen Zielpublikums anstelle des Azure-Ressourcenzielpublikums aktualisiert.
    * Fehler korrigiert, der die Größe von Dateien einschränkt, die mit den folgenden Cmdlets erstellt/angefügt werden:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* Dns
    * Fehler im Pipingszenario für „Get-AzureRmDnsZone“ korrigiert
        - Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Unterstützung zum Aktivieren/Deaktivieren von Operations Management Suite (OMS) hinzugefügt
    * Neue Cmdlets
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Neue Parameter zum Festlegen von benutzerdefinierten Spark-Konfigurationen für „Add-AzureRmHDInsightConfigValues“
        - Parameter „SparkDefaults“ und „SparkThriftConf“ für Spark 1.6
        - Parameter „Spark2Defaults“ und „Spark2ThriftConf“ für Spark 2.0
* Einblicke
    * Problem 4215 (Änderungsanforderung) gelöst: 15-Tage-Limit im Zeitfenster für das Cmdlet „Get-AzureRmLog“ entfernt. Darüber hinaus wurden kleinere Änderungen an den Namen von Komponententests vorgenommen.
    * Problem 3957 für „Get-AzureRmLog“ gelöst.
        - Problem 1: Das Back-End gibt die Datensätze in Seiten mit je 200 Einträgen zurück, das Fortsetzungstoken verknüpft mit der nächsten Seite. Die Kunden konnten über das Cmdlet nur 200 Einträge anzeigen, obwohl sie wussten, dass mehr Einträge vorlagen. Dieses Verhalten trat unabhängig davon auf, welcher Wert für „MaxEvents“ festgelegt wurde – es sei denn, der Wert lag unter 200.
        - Problem 2: Die Dokumentation enthielt falsche Angaben zu diesem Cmdlet, z.B. lautete das Standardzeitfenster 1 Stunde.
        - Fix 1: Das Cmdlet folgt jetzt dem vom Back-End zurückgegebenen Fortsetzungstoken, bis „MaxEvents“ oder das Ende des Satzes erreicht wurde.<br>Der Standardwert für „MaxEvents“ lautet 1000, der maximal zulässige Wert ist 100000. Jeder Wert für „MaxEvents“, der unter 1 liegt, wird ignoriert. Stattdessen wird der Standardwert verwendet. Diese Werte und dieses Verhalten haben sich nicht geändert, aber jetzt sind sie richtig dokumentiert.<br>Für „MaxEvents“ wurde der Alias „-MaxRecords-“ hinzugefügt, weil der Name des Cmdlets nur noch auf Protokolle, aber nicht mehr auf Ereignisse verweist.
        - Fix 2: Die Dokumentation enthält richtige und ausführlichere Informationen: neuer Alias, richtiges Zeitfenster, richtige Standard-, Mindest- und Höchstwerte.
* KeyVault
    * Entfernt die E-Mail-Adresse aus der Verzeichnisabfrage, wenn für die Cmdlets „Set-AzureRMKeyVaultAccessPolicy“ und „Remove-AzureRMKeyVaultAccessPolicy“ der Parameter „UserPrincipalName“ angegeben wird.
      - Beide Cmdlets verfügen jetzt über einen Parameter „-EmailAddress“, der anstelle von „-UserPrincipalName“ verwendet werden kann, wenn eine E-Mail-Abfrage geeignet ist.  Wenn mehr als eine übereinstimmende E-Mail-Adresse vorhanden ist, kommt es bei dem Cmdlet zu einem Fehler.
* Netzwerk
    * New-AzureRmIpsecPolicy: „SALifeTimeSeconds“ und „SADataSizeKilobytes“ sind nicht länger erforderliche Parameter.
        - Standardwert für „SALifeTimeSeconds“: 27000 Sekunden
        - Standardwert für „SADataSizeKilobytes“: 102400000 KB
    * Unterstützung für die Konfiguration benutzerdefinierter Verschlüsselungssammlungen über die SSL-Richtlinie und für das Auflisten aller SSL-Optionen-APIs in Application Gateway
        - Optionale Parameter „-PolicyType“, „-PolicyName“, „-MinProtocolVersion“ und „-Ciphersuite“ hinzugefügt
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - „Get-AzureRmApplicationGatewayAvailableSslOptions“ hinzugefügt (Alias: List-AzureRmApplicationGatewayAvailableSslOptions)
        - „Get-AzureRmApplicationGatewaySslPredefinedPolicy“ hinzugefügt (Alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Umleitungsunterstützung in Application Gateway hinzugefügt
        - „Add-AzureRmApplicationGatewayRedirectConfiguration“ hinzugefügt
        - „Get-AzureRmApplicationGatewayRedirectConfiguration“ hinzugefügt
        - „New-AzureRmApplicationGatewayRedirectConfiguration“ hinzugefügt
        - „Remove-AzureRmApplicationGatewayRedirectConfiguration“ hinzugefügt
        - „Set-AzureRmApplicationGatewayRedirectConfiguration“ hinzugefügt
        - Optionaler Parameter „-RedirectConfiguration“ hinzugefügt
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Optionaler Parameter „-DefaultRedirectConfiguration“ hinzugefügt
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Optionaler Parameter „-RedirectConfiguration“ hinzugefügt
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Optionaler Parameter „-RedirectConfigurations“ hinzugefügt
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Unterstützung für Azure Websites in Application Gateway hinzugefügt
        - „New-AzureRmApplicationGatewayProbeHealthResponseMatch“ hinzugefügt
        - Optionale Parameter „-PickHostNameFromBackendHttpSettings“, „-MinServers“ und „ -Match“ hinzugefügt
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Optionale Parameter „-PickHostNameFromBackendAddress“, „-AffinityCookieName“, „-ProbeEnabled“ und „-Path“ hinzugefügt
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * „Get-AzureRmPublicIPaddress“ aktualisiert, um publicipaddress-Ressourcen abzurufen, die über eine VM-Skalierungsgruppe erstellt wurden
    * Cmdlet zum Abrufen der aktuellen Nutzung eines virtuellen Netzwerks hinzugefügt
        - Get-AzureRmVirtualNetworkUsageList
* Profil
    * Fehler bei Verwendung von „Import-AzureRmContext“ oder „Save-AzureRmContext“ behoben
        - Weitere Informationen finden Sie unter diesem Problem: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Neues Modul für Azure Site Recovery-Vorgänge eingeführt.
        - Alle Cmdlets beginnen mit „AzureRmRecoveryServicesAsr*“.
* Sql
    * PowerShell-Cmdlets für die Datensynchronisierung zu „AzureRM.Sql“ hinzugefügt
    * AzureRmSqlServer-Cmdlets für die Verwendung der neuen REST-API-Version aktualisiert, die Timeouts beim Erstellen des Servers verhindert.
    * Cmdlets für ein Serverupgrade eingestellt, weil die alte Serverversion (2.0) nicht mehr vorhanden ist.
    * Neuer optionaler Parameter „AssignIdentity“ zu den Cmdlets „New-AzureRmSqlServer“ und „Set-AzureRmSqlServer“ hinzugefügt, um die Bereitstellung einer Ressourcenidentität für die SQL Server-Ressource zu unterstützen
    * Parameter „ResourceGroupName“ ist für Get-AzureRmSqlServer jetzt optional
        - Weitere Informationen finden Sie unter dem folgenden Problem: https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement für ExpressRoute:
    * Cmdlet „New-AzureBgpPeering“ aktualisiert, um folgende neue Optionen hinzuzufügen:
        - PeerAddressType: Werte „IPv4“ oder „IPv6“ ermöglichen das Erstellen eines BGP-Peerings mit dem entsprechenden Adressfamilientyp
    * Cmdlet „Set-AzureBgpPeering“ aktualisiert, um folgende neue Optionen hinzuzufügen:
        - PeerAddressType: Werte „IPv4“ oder „IPv6“ ermöglichen das Aktualisieren eines BGP-Peerings mit dem entsprechenden Adressfamilientyp
    * Cmdlet „Remove-AzureBgpPeering“ aktualisiert, um folgende neue Optionen hinzuzufügen:
        - PeerAddressType: Werte „IPv4“, „IPv6“ oder „All“ ermöglichen eine Entfernung des BGP-Peerings mit dem entsprechenden Adressfamilientyp oder aller BGP-Peerings

## <a name="20170607---version-410"></a>2017.06.07 – Version 4.1.0
* AnalysisServices
    * Neue SKUs hinzugefügt: B1, B2, S0
    * Unterstützung zum Hoch-/Herunterskalieren hinzugefügt
* CognitiveServices
    * Detaillierte Anzeige der Lizenzvereinbarungen beim Erstellen von Cognitive Services-Ressourcen aktualisiert
* Compute
    * Korrektur von „Test-AzureRmVMAEMExtension“ für virtuelle Computer mit mehreren verwalteten Datenträgern
    * „Set-AzureRmVMAEMExtension“ aktualisiert: Cachinginformationen für verwaltete Premium-Datenträger hinzugefügt
    * Add-AzureRmVhd: Das Größenlimit für VHD wurde auf 4 TB erhöht.
    * Stop-AzureRmVM: Dokumentation für den Parameter „STayProvisioned“ klarer formuliert
    * New-AzureRmDiskUpdateConfig
      * Eingestellte Parameter: CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmDiskUpdateImageReference: Veraltetes Cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * Eingestellte Parameter: CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference: Veraltetes Cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Verwaltete KeyVault-Verschlüsselung für DataLake Store aktiviert
* DevTestLabs
    * Cmdlets aktualisiert, um mit der aktuellen und der aktualisierten DevTest-Labs-API-Version arbeiten zu können.
* IotHub
    * Routingunterstützung für IoTHub-Cmdlets hinzugefügt
* KeyVault
  * Neue Cmdlets zur Unterstützung von KeyVault-Schlüsseln für verwaltete Speicherkonten
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Netzwerk
    * Get-AzureRmNetworkUsage: Neues Cmdlet zur Anzeige von Netzwerknutzung und Kapazitätsdetails
    * Neue GatewaySku-Optionen für „VirtualNetworkGateways“ hinzugefügt
        * VpnGw1, VpnGw2, VpnGw3 als neue SKUs für VPN-Gateways hinzugefügt
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Hilfebeispiele korrigiert
* Notification Hubs
    * Transparentes Update der NotificationHubs-Cmdlets für neue API
* Profil
    * Resolve-AzureRmError
      * Neue Cmdlets zur Anzeige von Details zu Fehlern und Ausnahmen, die von Cmdlets ausgegeben werden (einschließlich Serveranforderung/Antwortdaten)
    * Send-Feedback
      * Möglichkeit zum Senden von Feedback ohne Anmeldung
    * Get-AzureRmSubscription
      * Fehler beim Abruf von CSP-Abonnements korrigiert
* Ressourcen
    * Problem behoben, bei dem „Get-AzureRMRoleAssignment“ zu einer ungültigen Anforderung führt, wenn die Anzahl von Rollenzuweisungen über 1000 liegt
        * Benutzer können jetzt „Get-AzureRMRoleAssignment“ selbst dann verwenden, wenn mehr als 1000 Zuweisungen zurückgegeben werden müssen
* Sql
    * Restore-AzureRmSqlDatabase: Dokumentationsbeispiel aktualisiert
* Storage
    * Unterstützung für Einstellung „AssignIdentity“ zu Cmdlets für Speicherkonten mit Ressourcenmodus hinzugefügt
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Unterstützung zum Hinzufügen eines Kundenschlüssels zu Cmdlets für Speicherkonten mit Ressourcenmodus hinzugefügt
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* Traffic Manager

    * Neue Monitoreinstellungen „MonitorIntervalInSeconds“, „MonitorTimeoutInSeconds“, „MonitorToleratedNumberOfFailures“
    * Neues Monitorprotokoll „TCP“
* ServiceManagement
    * Add-AzureVhd: Das Größenlimit für VHD wurde auf 4 TB erhöht.
    * New-AzureBGPPeering: Unterstützung für „LegacyMode“
* Azure.Storage
    * Hilfe zu Parametern aktualisiert, die Platzhalterzeichen akzeptieren, StorageContext-Typ aktualisiert

## <a name="20170523---version-402"></a>2017.05.23 – Version 4.0.2
* Profil
    * Add-AzureRmAccount
      * Parameteralias `-EnvironmentName` zur Abwärtskompatibilität mit 2.x-Versionen von „AzureRM.profile“ hinzugefügt

## <a name="20170512---version-401"></a>2017.05.12 – Version 4.0.1
 * Problem mit „New-AzureStorageContext“ in Offlineszenarien behoben: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 – Version 4.0.0


* Diese Version enthält wichtige Änderungen. Im [Migrationshandbuch](https://aka.ms/azps-migration-guide) finden Sie Änderungsdetails sowie die Auswirkung auf vorhandene Skripts.
* ApiManagement
  - Unterstützung für das Konfigurieren externer Gruppen in „New-AzureRmApiManagementGroup“ hinzugefügt.
* Abrechnung
  - Neues Cmdlet „Get-AzureRmBillingPeriod“
    + Cmdlet zum Abrufen von Azure-Abrechnungszeiträumen im Abonnement.
  - Cmdlet „Get-AzureRmBillingInvoice“ aktualisiert
  - Neue Eigenschaft „BillingPeriodNames“
  - Ausgabe in Listenansicht
* Compute
  - Cmdlets „Set-AzureRmVMAEMExtension“ und „Test-AzureRmVMAEMExtension“ für die Unterstützung von Premium Managed Disks aktualisiert
  - Sichern von Verschlüsselungseinstellungen für IaaS-VMs und Wiederherstellen bei einem Fehler
  - Die Option „ChefServiceInterval“ wurde in „ChefDaemonInterval“ umbenannt. Die alte Bezeichnung funktioniert jedoch weiterhin.
  - Die duplizierten Eigenschaften „DataDiskNames“ und „NetworkInterfaceIDs“ wurden aus dem PowerShell-Objekt „VM“ entfernt.
  - Die Parameter „DataDiskNames“ und „NetworkInterfaceIDs“ wurden in „Remove-AzureRmVMDataDisk“ bzw. „Remove-AzureRmVMNetworkInterface“ in optional geändert.
  - Das Weiterleitungsproblem von „Get“-Cmdlets, wenn diese ein Listenobjekt zurückgeben, wurde behoben.
  - Cmdlets, die in Konflikt mit RDFE-Cmdlets stehen, wurden umbenannt. Ausführlichere Informationen unter diesem Problem: https://github.com/Azure/azure-powershell/issues/2917
    + `New-AzureVMSqlServerAutoBackupConfig` wurde in `New-AzureRmVMSqlServerAutoBackupConfig` umbenannt.
    + `New-AzureVMSqlServerAutoPatchingConfig` wurde in `New-AzureRmVMSqlServerAutoPatchingConfig` umbenannt.
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` wurde in `New-AzureRmVMSqlServerKeyVaultCredentialConfig` umbenannt.
* Nutzung
  - Neues Cmdlet „Get-AzureRmConsumptionUsageDetail“
    + Cmdlet zum Abrufen der Nutzungsdetails des Abonnements.
* ContainerRegistry
  - PowerShell-Cmdlets für Azure-Containerregistrierung hinzugefügt
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Unterstützung für „get“ und „list“ für Katalogpaket hinzugefügt
  - Unterstützung für das Auflisten der folgenden Katalogelemente aus tieferen Vorgängern hinzugefügt:
    + Tabelle
    + Tabellenwertfunktion (TVF)
    + Sicht
    + Statistik
* DataLakeStore
  - Für `Import-AzureRMDataLakeStoreItem` und `Export-AzureRMDataLakeStoreItem` wurde die Ablaufverfolgungsprotokollierung zur Verbesserung der Leistung standardmäßig deaktiviert. Wenn die Ablaufprotokollierung gewünscht ist, verwenden Sie die Parameter `-DiagnosticLogLevel` und `-DiagnosticLogPath`
  - Fehler korrigiert, der mitunter den Absturz von PowerShell verursachte, wenn viele kleine Dateien in AD LS hochgeladen wurden.
* EventHub
  - Fehlerbehebung:
    + Korrektur für Fehler im Cmdlet „Set-AzureRmEventHubNamespace“: 'Tarif' darf nicht NULL sein, wenn es 'SKU-Name' sein sollte
    + Set-AzureRmEventHub: Korrektur für den Fehler „Der Objektverweis ist nicht auf eine Objektinstanz festgelegt“ beim Aktualisieren von EventHub
* Einblicke
  - Add-AzureRm*AlertRule
    + Gibt ein einzelnes Objekt zurück: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + Die Ausgabe wird jetzt aufgezählt und nicht mehr als einzelnes Objekt betrachtet. Der Typ wurde nicht geändert, es ist immer noch eine Liste.
  - Remove-AzureRmAlertRule
    + Auf den Statuscode folgt der von der Anforderung zurückgegebene Statuscode. Vorher war dieser stets „OK“.
  - Add-AzureRmAutoscaleSetting
    + Gibt jetzt ein einzelnes Objekt (keine Liste wie zuvor) mit „statusCode“, „requestId“ und der neu erstellten/aktualisierten Ressource zurück.
    + Auf den Statuscode folgt der von der Anforderung zurückgegebene Status. Vorher war dieser stets „OK“.
  - New-AzureRmAutoscaleRule
    + Der Parameter „ScaleActionType“ wurde erweitert und empfängt nun die folgenden Werte: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + Auf den Statuscode in der Ausgabe folgt der von der Anforderung zurückgegebene Statuscode. Vorher war dieser stets „OK“.
  - Get-AzureRmLogProfile
    + Die Ausgabe wird jetzt aufgezählt. Zuvor wurde sie als einzelnes Objekt betrachtet. Der Typ der Ausgabe bleibt wie zuvor eine Liste.
  - Remove-AzureRmLogProfile
    + Der Parameter „PassThru“ wurde implementiert.
  - Metrik-API
    + Das SDK ruft nun Metriken aus der Masterdatenverwaltung (MDM) ab.
  - Get-AzureRmMetricDefinition
    + Die Ausgabe ist weiterhin eine Liste, aber die Struktur der Liste hat sich geändert.
  - Get-AzureRmMetric
    + Der Aufruf wurde geändert. Die neue Syntax lautet: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + Die Ausgabe ist eine Liste, und die Struktur der Elemente hat sich geändert.
* KeyVault
  - Unterstützung für die Sicherung/Wiederherstellung von KeyVault-Geheimnissen hinzugefügt
    + Geheimnisse können entsprechend der derzeit für Schlüssel unterstützten Funktionen gesichert und wiederhergestellt werden

  - Cmdlets für die Sicherung von Schlüsseln und Geheimnissen akzeptieren nun ein entsprechendes Objekt als Eingabeparameter
    + Der Aufrufer kann Abruf- und Sicherungsvorgänge verketten: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - Cmdlets für die Sicherung unterstützen nun den Schalter „-Force“, um eine vorhandene Datei zu überschreiben
    + Beachten Sie, dass beim Versuch des Überschreibens einer vorhandenen Datei keine Ausnahme mehr ausgelöst wird, sondern der Benutzer zur Entscheidung aufgefordert wird, wie fortgefahren werden soll.
* LogicApp
  - Neue Parameter für Cmdlets für die Notfallwiederherstellung von Austauschkontrollnummern:
    + Optionaler Parameter „-AgreementType“ (X12 oder Edifact) zum Angeben der relevanten Kontrollnummern
* MachineLearning
  - Neue Version des Azure Machine Learning .NET SDK wird genutzt, und ein neues Cmdlet wurde hinzugefügt
    + Add-AzureRmMlWebServiceRegionalProperty
  - Kleinere Formulierungskorrekturen im Hilfetext.
* Netzwerk
  - Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ hinzugefügt
    + Gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück
    + Wenn die Verbindung zwischen Quelle und Ziel nicht hergestellt werden kann, gibt das Cmdlet Einzelheiten zum Problem zurück
* Profil
  - Cmdlet „Send-Feedback“ hinzugefügt: Ermöglicht einem Benutzer das Auslösen einer Reihe von Aufforderungen zum Senden von Feedback an das Azure PowerShell-Team.
  - Die folgenden Aliase wurden entfernt, da sie mit vorhandenen Cmdlet-Namen im Azure-Modul in Konflikt stehen:
    + `Enable-AzureDataCollection` (unterstützt von `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (unterstützt von `Disable-AzureRmDataCollection`)
* Relay
  - Cmdlets für Azure Relay hinzugefügt, die Benutzern das Erstellen und Verwalten sämtlicher Azure Relay-Ressourcen erlauben.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Ressourcen
  - Unterstützung für ressourcengruppenübergreifende Bereitstellungen für „New-AzureRmResourceGroupDeployment“
    + Benutzer können jetzt geschachtelte Bereitstellungen verwenden, um verschiedene Ressourcengruppen bereitzustellen.
* ServiceBus

  - Fehlerbehebung: Eigenschaftswerte des ServiceBus-Warteschlangenobjekts wurden auf NULL festgelegt. Das Objekt wird als Eingabeparameter im Cmdlet „Set-AzureRmServiceBusQueue“ verwendet, um die Warteschlange zu aktualisieren.
    - Betroffene Eigenschaften: LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount und MessageCount
* ServiceFabric

  - Cmdlets für Service Fabric hinzugefügt
    + Add-AzureRmServiceFabricApplicationCertificate: Fügt ein Zertifikat hinzu, das als Anwendungszertifikat verwendet wird
    + Add-AzureRmServiceFabricClientCertificate: Fügt den Clustereinstellungen einen allgemeinen Namen oder Fingerabdruck für die Clientauthentifizierung hinzu
    + Add-AzureRmServiceFabricClusterCertificate: Fügt dem Cluster ein sekundäres Clusterzertifikat hinzu, um das vorhandene Zertifikat zu verlängern
    + Add-AzureRmServiceFabricNodes: Fügt einem Cluster Knoten/VMs eines bestimmten Knotentyps hinzu
    + Add-AzureRmServiceFabricNodeType: Fügt einem vorhandenen Cluster einen Knotentyp bzw. VMs hinzu
    + Get-AzureRmServiceFabricCluster: Ruft die Details der Clusterressource ab
    + New-AzureRmServiceFabricCluster: Erstellt einen neuen ServiceFabric-Cluster. Dieser Befehl hat viele Überladungen, um verschiedene Szenarien abzudecken
    + Remove-AzureRmServiceFabricClientCertificate: Entfernt ein Clientzertifikat, damit es nicht für den Zugriff auf einen Cluster verwendet wird
    + Remove-AzureRmServiceFabricClusterCertificate: Entfernt ein Clusterzertifikat, damit es nicht für die Clustersicherheit verwendet wird
    + Remove-AzureRmServiceFabricNodes: Entfernt Knoten eines bestimmten Knotentyps aus einem Cluster
    + Remove-AzureRmServiceFabricNodeType: Entfernt einen Knotentyp aus einem Cluster
    + Remove-AzureRmServiceFabricSettings: Entfernt eine oder mehrere ServiceFabric-Einstellungen aus einem Cluster
    + Set-AzureRmServiceFabricSettings: Dient zum Hinzufügen oder Aktualisieren einer oder mehrerer ServiceFabric-Einstellungen eines Clusters
    + Set-AzureRmServiceFabricUpgradeType: Ändert den ServiceFabric-Upgradetyp eines Clusters
    + Update-AzureRmServiceFabricDurability: Ändert die Dauerhaftigkeitsstufe eines Clusters
    + Update-AzureRmServiceFabricReliability: Ändert die Zuverlässigkeitsstufe eines Clusters
* Sql
  - „New-AzureRmSqlDatabase“ wurde der Parameter „-SampleName“ hinzugefügt
  - Updates für Failovergruppen-Cmdlets
  - „Tag“-Parameter entfernt
  - Aus dem Cmdlet „Remove-AzureRmSqlDatabaseFailoverGroup“ wurden die Parameter „PartnerResourceGroupName“ und „PartnerServerName“ entfernt
  - Den Cmdlets „New-“ und „Set-“ wurde der Parameter „GracePeriodWithDataLossHours“ hinzugefügt, durch den „GracePeriodWithDataLossHour“ letztendlich ersetzt wird
  - Dokumentation wurde konkretisiert und aktualisiert
  - Die Formatierung zurückgegebener Objekte wurde geändert, und einige Fehler wurden behoben, bei denen Felder nicht immer aufgefüllt wurden
  - Dem Objekt „FailoverGroup“ wurden die Eigenschaften „DatabaseNames“ und „PartnerLocation“ hinzugefügt
  - Korrektur eines Fehlers, der bewirkte, dass das Cmdlet „Switch-“ sofort eine Rückgabe lieferte, anstatt auf den Abschluss des Vorgangs zu warten
  - Überlauffehler bei ganzen Zahlen behoben, wenn hohe Werte für die Toleranzperiode verwendet werden
  - Die Toleranzperiode wird auf mindestens 1 Stunde angepasst, wenn eine kürzere angegeben wird
  - „Usage_Anomaly“ aus den akzeptierten Werten für den Parameter „ExcludedDetectionType“ für die Cmdlets „Set-AzureRmSqlDatabaseThreatDetectionPolicy“ und „Set-AzureRmSqlServerThreatDetectionPolicy“ entfernt.
* Storage
  - Aktualisierung des SRP SDK auf 6.3.0
  - New/Set-AzureRmStorageAccount: Neuen Parameter zur Unterstützung von „EnableHttpsTrafficOnly“ hinzugefügt
  - New/Set/Get-AzureRmStorageAccount: Zurückgegebenes Speicherkonto enthält das neue Attribut „EnableHttpsTrafficOnly“
* Azure.Storage
  - Upgrade auf Azure Storage-Clientbibliothek 8.1.1 und Azure Storage DataMovement-Bibliothek 0.5.1
  - Neues Cmdlet zum Unterstützen der Blobfunktion „Inkrementelles Kopieren“
