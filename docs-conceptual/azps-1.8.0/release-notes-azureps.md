---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 7d468fb760f9be23e8b8eea7f74adc1dd137e469
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408325"
---
# <a name="azure-powershell-release-notes"></a>Versionshinweise zu Azure PowerShell
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
