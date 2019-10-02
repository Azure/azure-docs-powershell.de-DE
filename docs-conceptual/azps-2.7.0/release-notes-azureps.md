---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319309"
---
## <a name="270---september-2019"></a><span data-ttu-id="a258e-103">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a258e-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a258e-104">Az.ApiManagement</span></span>
* <span data-ttu-id="a258e-105">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a258e-106">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="a258e-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a258e-107">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="a258e-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-108">Az.Automation</span></span>
* <span data-ttu-id="a258e-109">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a258e-110">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a258e-111">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-112">Az.Compute</span></span>
* <span data-ttu-id="a258e-113">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a258e-114">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a258e-115">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a258e-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a258e-116">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a258e-117">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a258e-118">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="a258e-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a258e-119">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a258e-120">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a258e-121">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-122">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-123">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a258e-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a258e-124">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a258e-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a258e-125">Az.HDInsight</span></span>
* <span data-ttu-id="a258e-126">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a258e-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a258e-127">Az.IotHub</span></span>
* <span data-ttu-id="a258e-128">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a258e-129">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a258e-130">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a258e-130">New cmdlets are:</span></span>
    - <span data-ttu-id="a258e-131">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a258e-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a258e-132">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a258e-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a258e-133">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a258e-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a258e-134">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a258e-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a258e-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-135">Az.Monitor</span></span>
* <span data-ttu-id="a258e-136">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="a258e-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a258e-137">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="a258e-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a258e-138">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a258e-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a258e-139">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="a258e-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a258e-140">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="a258e-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a258e-141">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="a258e-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a258e-142">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a258e-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a258e-143">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a258e-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a258e-144">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="a258e-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a258e-145">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a258e-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a258e-146">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="a258e-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a258e-147">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a258e-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a258e-148">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="a258e-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a258e-149">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="a258e-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a258e-150">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="a258e-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a258e-151">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="a258e-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a258e-152">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="a258e-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a258e-153">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="a258e-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a258e-154">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a258e-155">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="a258e-155">Overall improved help files</span></span>
* <span data-ttu-id="a258e-156">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-157">Az.Network</span></span>
* <span data-ttu-id="a258e-158">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="a258e-159">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a258e-160">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="a258e-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a258e-161">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="a258e-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a258e-162">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a258e-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a258e-163">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a258e-164">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a258e-165">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a258e-166">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a258e-167">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a258e-168">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a258e-169">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="a258e-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a258e-170">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-170">New cmdlets</span></span>
        - <span data-ttu-id="a258e-171">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a258e-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a258e-172">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a258e-173">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a258e-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="a258e-174">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a258e-174">New-VpnSite</span></span>
        - <span data-ttu-id="a258e-175">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a258e-175">Update-VpnSite</span></span>
        - <span data-ttu-id="a258e-176">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-176">New-VpnConnection</span></span>
        - <span data-ttu-id="a258e-177">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-177">Update-VpnConnection</span></span>
* <span data-ttu-id="a258e-178">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a258e-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-180">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a258e-181">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-182">Az.Resources</span></span>
* <span data-ttu-id="a258e-183">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="a258e-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a258e-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-185">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a258e-186">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a258e-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a258e-187">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a258e-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a258e-188">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a258e-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a258e-189">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a258e-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a258e-190">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a258e-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a258e-191">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a258e-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a258e-192">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a258e-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a258e-193">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a258e-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a258e-194">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a258e-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a258e-195">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a258e-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a258e-196">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a258e-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a258e-197">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a258e-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a258e-198">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a258e-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a258e-199">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a258e-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a258e-200">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="a258e-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a258e-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a258e-201">Az.SignalR</span></span>
* <span data-ttu-id="a258e-202">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-203">Az.Sql</span></span>
* <span data-ttu-id="a258e-204">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a258e-205">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="a258e-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a258e-206">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="a258e-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a258e-207">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a258e-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a258e-208">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="a258e-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-209">Az.Storage</span></span>
* <span data-ttu-id="a258e-210">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a258e-211">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a258e-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a258e-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a258e-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a258e-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a258e-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a258e-214">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a258e-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a258e-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a258e-216">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="a258e-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a258e-217">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a258e-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a258e-218">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a258e-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a258e-219">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a258e-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a258e-220">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a258e-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-221">Az.Websites</span></span>
* <span data-ttu-id="a258e-222">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="a258e-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a258e-223">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a258e-224">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a258e-225">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a258e-226">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a258e-226">General</span></span>
* <span data-ttu-id="a258e-227">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a258e-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-228">Az.Accounts</span></span>
* <span data-ttu-id="a258e-229">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="a258e-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a258e-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a258e-230">Az.Aks</span></span>
* <span data-ttu-id="a258e-231">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a258e-232">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a258e-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a258e-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a258e-233">Az.ApiManagement</span></span>
* <span data-ttu-id="a258e-234">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a258e-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a258e-235">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="a258e-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a258e-236">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a258e-237">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a258e-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a258e-238">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a258e-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a258e-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a258e-239">Az.Batch</span></span>
* <span data-ttu-id="a258e-240">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="a258e-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a258e-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a258e-241">Az.Cdn</span></span>
* <span data-ttu-id="a258e-242">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-243">Az.Compute</span></span>
* <span data-ttu-id="a258e-244">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a258e-245">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a258e-246">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a258e-247">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a258e-248">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a258e-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a258e-249">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a258e-250">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a258e-251">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-252">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-253">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="a258e-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a258e-254">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a258e-255">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a258e-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a258e-256">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-258">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a258e-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a258e-259">Az.EventHub</span></span>
* <span data-ttu-id="a258e-260">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="a258e-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a258e-261">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="a258e-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a258e-262">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a258e-263">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="a258e-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a258e-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a258e-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a258e-265">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a258e-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-266">Az.Monitor</span></span>
* <span data-ttu-id="a258e-267">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-268">Az.Network</span></span>
* <span data-ttu-id="a258e-269">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a258e-270">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="a258e-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a258e-271">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="a258e-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a258e-272">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a258e-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a258e-273">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="a258e-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="a258e-274">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a258e-275">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="a258e-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="a258e-277">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="a258e-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a258e-278">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-278">Added example</span></span>
    - <span data-ttu-id="a258e-279">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a258e-280">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a258e-281">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-283">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-284">Az.Resources</span></span>
* <span data-ttu-id="a258e-285">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a258e-286">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a258e-287">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a258e-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a258e-288">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a258e-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a258e-289">Az.ServiceBus</span></span>
* <span data-ttu-id="a258e-290">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="a258e-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a258e-291">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="a258e-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a258e-292">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="a258e-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-294">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="a258e-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a258e-295">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="a258e-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a258e-296">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a258e-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a258e-297">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="a258e-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a258e-298">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a258e-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a258e-299">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="a258e-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-300">Az.Sql</span></span>
* <span data-ttu-id="a258e-301">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-302">Az.Storage</span></span>
* <span data-ttu-id="a258e-303">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="a258e-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a258e-304">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="a258e-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a258e-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a258e-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a258e-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a258e-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a258e-307">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="a258e-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a258e-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a258e-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-309">Az.Websites</span></span>
* <span data-ttu-id="a258e-310">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="a258e-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a258e-311">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-312">Az.Accounts</span></span>
* <span data-ttu-id="a258e-313">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a258e-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a258e-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a258e-315">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="a258e-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-316">Az.Automation</span></span>
* <span data-ttu-id="a258e-317">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="a258e-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a258e-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="a258e-319">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-320">Az.Compute</span></span>
* <span data-ttu-id="a258e-321">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a258e-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a258e-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a258e-323">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a258e-324">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="a258e-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-325">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-326">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a258e-327">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a258e-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a258e-328">Az.EventHub</span></span>
* <span data-ttu-id="a258e-329">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a258e-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a258e-330">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="a258e-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a258e-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a258e-331">Az.KeyVault</span></span>
* <span data-ttu-id="a258e-332">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a258e-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a258e-333">Az.LogicApp</span></span>
* <span data-ttu-id="a258e-334">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="a258e-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a258e-335">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a258e-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a258e-336">Az.ManagedServices</span></span>
* <span data-ttu-id="a258e-337">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-338">Az.Network</span></span>
* <span data-ttu-id="a258e-339">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a258e-340">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-340">New cmdlets</span></span>
        - <span data-ttu-id="a258e-341">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a258e-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a258e-342">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a258e-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a258e-343">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a258e-344">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a258e-345">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a258e-346">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a258e-347">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a258e-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a258e-348">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a258e-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a258e-349">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a258e-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a258e-350">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a258e-351">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a258e-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a258e-352">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a258e-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a258e-353">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a258e-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a258e-354">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="a258e-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a258e-355">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-355">Updated cmdlets</span></span>
        - <span data-ttu-id="a258e-356">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a258e-357">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a258e-358">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a258e-359">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a258e-360">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a258e-361">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a258e-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="a258e-362">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a258e-363">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a258e-364">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a258e-365">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a258e-366">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a258e-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a258e-367">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="a258e-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="a258e-369">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="a258e-370">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-372">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a258e-373">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a258e-374">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a258e-375">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a258e-376">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a258e-377">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a258e-378">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a258e-379">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a258e-380">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a258e-381">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-382">Az.Resources</span></span>
- <span data-ttu-id="a258e-383">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="a258e-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a258e-384">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a258e-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a258e-385">Az.ServiceBus</span></span>
* <span data-ttu-id="a258e-386">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a258e-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a258e-387">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="a258e-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-388">Az.Sql</span></span>
* <span data-ttu-id="a258e-389">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a258e-390">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a258e-391">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-392">Az.Storage</span></span>
* <span data-ttu-id="a258e-393">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a258e-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a258e-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a258e-394">Az.StorageSync</span></span>
* <span data-ttu-id="a258e-395">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a258e-396">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-397">Az.Websites</span></span>
* <span data-ttu-id="a258e-398">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="a258e-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a258e-399">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a258e-400">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a258e-401">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-402">Az.Accounts</span></span>
* <span data-ttu-id="a258e-403">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a258e-404">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a258e-405">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="a258e-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a258e-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a258e-406">Az.Advisor</span></span>
* <span data-ttu-id="a258e-407">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a258e-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a258e-408">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="a258e-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a258e-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a258e-409">Az.ApiManagement</span></span>
* <span data-ttu-id="a258e-410">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a258e-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a258e-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a258e-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a258e-412">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a258e-413">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="a258e-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a258e-414">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a258e-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a258e-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a258e-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a258e-416">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-417">Az.Automation</span></span>
* <span data-ttu-id="a258e-418">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-419">Az.Compute</span></span>
* <span data-ttu-id="a258e-420">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-421">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-422">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a258e-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a258e-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a258e-423">Az.EventGrid</span></span>
* <span data-ttu-id="a258e-424">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a258e-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a258e-425">Az.IotHub</span></span>
* <span data-ttu-id="a258e-426">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-427">Az.Network</span></span>
* <span data-ttu-id="a258e-428">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a258e-429">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a258e-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a258e-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="a258e-431">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a258e-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a258e-432">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a258e-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="a258e-434">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-436">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="a258e-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-437">Az.Resources</span></span>
    - <span data-ttu-id="a258e-438">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a258e-439">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a258e-440">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a258e-441">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a258e-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a258e-442">Az.ServiceBus</span></span>
* <span data-ttu-id="a258e-443">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="a258e-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-444">Az.Sql</span></span>
* <span data-ttu-id="a258e-445">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a258e-446">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a258e-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a258e-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a258e-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a258e-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a258e-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a258e-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a258e-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a258e-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a258e-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a258e-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a258e-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a258e-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a258e-453">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-454">Az.Storage</span></span>
* <span data-ttu-id="a258e-455">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="a258e-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a258e-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a258e-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a258e-457">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="a258e-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a258e-458">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="a258e-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a258e-459">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a258e-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a258e-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a258e-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a258e-462">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="a258e-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a258e-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a258e-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a258e-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a258e-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a258e-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a258e-465">Az.StorageSync</span></span>
* <span data-ttu-id="a258e-466">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="a258e-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a258e-467">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-468">Az.Accounts</span></span>
* <span data-ttu-id="a258e-469">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="a258e-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a258e-470">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a258e-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a258e-471">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a258e-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a258e-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a258e-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a258e-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-474">Az.Compute</span></span>
* <span data-ttu-id="a258e-475">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="a258e-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a258e-476">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a258e-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a258e-477">Az.Dns</span></span>
* <span data-ttu-id="a258e-478">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a258e-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a258e-479">Az.EventGrid</span></span>
* <span data-ttu-id="a258e-480">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a258e-481">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a258e-481">New cmdlets:</span></span>
    - <span data-ttu-id="a258e-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a258e-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a258e-483">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="a258e-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a258e-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a258e-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a258e-485">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a258e-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a258e-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a258e-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a258e-487">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="a258e-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a258e-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a258e-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a258e-489">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="a258e-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a258e-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a258e-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a258e-491">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a258e-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a258e-492">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a258e-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a258e-493">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="a258e-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a258e-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a258e-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a258e-495">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a258e-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="a258e-496">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a258e-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a258e-497">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="a258e-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a258e-498">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a258e-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="a258e-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a258e-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a258e-500">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a258e-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a258e-501">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a258e-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a258e-502">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="a258e-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a258e-503">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a258e-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a258e-504">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="a258e-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a258e-505">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="a258e-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a258e-506">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a258e-507">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="a258e-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="a258e-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a258e-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a258e-509">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a258e-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a258e-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a258e-511">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a258e-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a258e-512">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a258e-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a258e-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a258e-513">Az.FrontDoor</span></span>
* <span data-ttu-id="a258e-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a258e-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a258e-515">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a258e-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a258e-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a258e-517">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-518">Az.Network</span></span>
* <span data-ttu-id="a258e-519">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a258e-520">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-520">New cmdlets</span></span>
        - <span data-ttu-id="a258e-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a258e-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a258e-522">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a258e-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a258e-523">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-523">New cmdlets</span></span> 
        - <span data-ttu-id="a258e-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a258e-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a258e-525">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a258e-526">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-526">New cmdlets</span></span> 
        - <span data-ttu-id="a258e-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a258e-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="a258e-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a258e-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a258e-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a258e-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a258e-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a258e-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a258e-532">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a258e-533">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-533">New cmdlets</span></span>
        - <span data-ttu-id="a258e-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a258e-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a258e-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a258e-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a258e-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a258e-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a258e-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a258e-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a258e-538">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="a258e-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a258e-539">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="a258e-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a258e-540">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="a258e-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a258e-541">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a258e-542">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a258e-543">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="a258e-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a258e-544">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a258e-545">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="a258e-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a258e-546">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a258e-547">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a258e-548">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="a258e-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a258e-549">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a258e-550">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a258e-551">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a258e-552">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="a258e-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a258e-553">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="a258e-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a258e-554">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="a258e-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a258e-555">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="a258e-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a258e-556">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="a258e-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="a258e-557">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="a258e-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="a258e-558">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a258e-559">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a258e-560">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="a258e-562">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="a258e-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-563">Az.Resources</span></span>
* <span data-ttu-id="a258e-564">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a258e-565">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a258e-566">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a258e-567">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a258e-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a258e-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-569">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="a258e-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-570">Az.Sql</span></span>
* <span data-ttu-id="a258e-571">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a258e-572">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a258e-573">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="a258e-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a258e-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a258e-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a258e-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a258e-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a258e-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a258e-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a258e-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a258e-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a258e-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a258e-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-579">Az.Storage</span></span>
* <span data-ttu-id="a258e-580">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a258e-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a258e-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="a258e-582">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="a258e-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a258e-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a258e-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-584">Az.Websites</span></span>
* <span data-ttu-id="a258e-585">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="a258e-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a258e-586">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a258e-587">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a258e-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a258e-588">Az.Cdn</span></span>
* <span data-ttu-id="a258e-589">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a258e-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-590">Az.Compute</span></span>
* <span data-ttu-id="a258e-591">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a258e-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a258e-592">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a258e-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a258e-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a258e-593">Az.EventHub</span></span>
* <span data-ttu-id="a258e-594">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="a258e-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a258e-595">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="a258e-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-596">Az.Network</span></span>
* <span data-ttu-id="a258e-597">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a258e-598">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a258e-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="a258e-600">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a258e-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-602">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a258e-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a258e-603">Az.ServiceBus</span></span>
* <span data-ttu-id="a258e-604">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="a258e-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a258e-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-606">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a258e-607">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-608">Az.Sql</span></span>
* <span data-ttu-id="a258e-609">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a258e-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a258e-610">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="a258e-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a258e-611">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="a258e-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a258e-612">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="a258e-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-613">Az.Websites</span></span>
* <span data-ttu-id="a258e-614">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a258e-615">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a258e-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a258e-616">Az.ApiManagement</span></span>
* <span data-ttu-id="a258e-617">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="a258e-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a258e-618">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="a258e-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a258e-619">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a258e-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a258e-620">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="a258e-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a258e-621">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="a258e-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a258e-622">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="a258e-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a258e-623">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a258e-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a258e-624">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a258e-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a258e-625">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="a258e-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a258e-626">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="a258e-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a258e-627">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="a258e-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a258e-628">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="a258e-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a258e-629">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="a258e-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a258e-630">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="a258e-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a258e-631">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="a258e-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a258e-632">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="a258e-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a258e-633">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="a258e-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a258e-634">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="a258e-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a258e-635">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="a258e-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="a258e-636">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="a258e-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a258e-637">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="a258e-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a258e-638">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="a258e-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a258e-639">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="a258e-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a258e-640">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="a258e-641">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a258e-642">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a258e-643">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="a258e-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a258e-644">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a258e-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a258e-645">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a258e-646">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="a258e-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a258e-647">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="a258e-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="a258e-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a258e-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a258e-649">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a258e-650">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a258e-651">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="a258e-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a258e-652">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a258e-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a258e-653">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a258e-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a258e-654">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="a258e-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a258e-655">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="a258e-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a258e-656">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="a258e-657">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="a258e-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a258e-658">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="a258e-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a258e-659">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="a258e-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a258e-660">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a258e-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a258e-661">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a258e-662">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="a258e-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a258e-663">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="a258e-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="a258e-664">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a258e-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a258e-665">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a258e-666">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="a258e-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a258e-667">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="a258e-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a258e-668">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="a258e-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a258e-669">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="a258e-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a258e-670">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a258e-671">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="a258e-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a258e-672">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="a258e-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a258e-673">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a258e-674">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a258e-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a258e-675">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a258e-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a258e-676">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a258e-677">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a258e-678">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a258e-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a258e-679">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a258e-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a258e-680">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a258e-681">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="a258e-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a258e-682">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="a258e-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a258e-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a258e-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a258e-684">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="a258e-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a258e-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a258e-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a258e-686">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a258e-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a258e-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a258e-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a258e-688">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a258e-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a258e-689">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="a258e-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a258e-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a258e-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a258e-691">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="a258e-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="a258e-692">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a258e-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a258e-693">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="a258e-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-694">Az.Automation</span></span>
* <span data-ttu-id="a258e-695">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a258e-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a258e-696">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a258e-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a258e-697">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a258e-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a258e-698">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="a258e-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a258e-699">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a258e-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a258e-700">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="a258e-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a258e-701">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="a258e-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-702">Az.Compute</span></span>
* <span data-ttu-id="a258e-703">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a258e-704">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="a258e-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-706">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="a258e-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a258e-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-707">Az.Monitor</span></span>
* <span data-ttu-id="a258e-708">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="a258e-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-709">Az.Network</span></span>
* <span data-ttu-id="a258e-710">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a258e-711">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a258e-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="a258e-712">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a258e-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a258e-713">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a258e-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-714">Az.Resources</span></span>
* <span data-ttu-id="a258e-715">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-716">Az.Sql</span></span>
* <span data-ttu-id="a258e-717">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="a258e-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a258e-718">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-719">Az.Accounts</span></span>
* <span data-ttu-id="a258e-720">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="a258e-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a258e-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a258e-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="a258e-722">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="a258e-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a258e-723">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="a258e-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-724">Az.Compute</span></span>
* <span data-ttu-id="a258e-725">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a258e-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a258e-726">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a258e-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a258e-727">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a258e-728">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a258e-729">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="a258e-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a258e-730">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="a258e-731">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="a258e-731">Breaking changes</span></span>
    - <span data-ttu-id="a258e-732">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a258e-733">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a258e-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a258e-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="a258e-735">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a258e-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a258e-736">Az.Dns</span></span>
* <span data-ttu-id="a258e-737">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="a258e-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a258e-738">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="a258e-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a258e-739">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a258e-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a258e-740">Az.FrontDoor</span></span>
* <span data-ttu-id="a258e-741">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a258e-742">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="a258e-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a258e-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a258e-743">Az.HDInsight</span></span>
* <span data-ttu-id="a258e-744">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="a258e-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a258e-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a258e-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a258e-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a258e-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a258e-747">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="a258e-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a258e-748">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="a258e-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a258e-749">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a258e-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a258e-750">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="a258e-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a258e-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-751">Az.Monitor</span></span>
* <span data-ttu-id="a258e-752">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="a258e-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="a258e-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a258e-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a258e-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a258e-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a258e-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a258e-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a258e-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a258e-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a258e-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a258e-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a258e-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a258e-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a258e-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a258e-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a258e-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a258e-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a258e-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a258e-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a258e-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a258e-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a258e-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a258e-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a258e-764">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="a258e-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a258e-765">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="a258e-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-766">Az.Network</span></span>
* <span data-ttu-id="a258e-767">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a258e-768">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-768">New cmdlets</span></span>
        - <span data-ttu-id="a258e-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a258e-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="a258e-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a258e-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a258e-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a258e-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a258e-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a258e-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a258e-773">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-773">Updated cmdlets</span></span>
        - <span data-ttu-id="a258e-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a258e-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a258e-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a258e-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a258e-776">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a258e-777">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="a258e-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a258e-778">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="a258e-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a258e-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="a258e-780">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="a258e-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a258e-781">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a258e-782">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="a258e-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-784">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="a258e-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a258e-785">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="a258e-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a258e-786">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="a258e-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a258e-787">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="a258e-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a258e-788">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="a258e-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a258e-789">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="a258e-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a258e-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a258e-790">Az.Relay</span></span>
* <span data-ttu-id="a258e-791">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="a258e-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a258e-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a258e-792">Az.ServiceBus</span></span>
* <span data-ttu-id="a258e-793">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-794">Az.Storage</span></span>
* <span data-ttu-id="a258e-795">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="a258e-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a258e-796">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a258e-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a258e-797">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a258e-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="a258e-799">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="a258e-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a258e-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a258e-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a258e-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-803">Az.Websites</span></span>
* <span data-ttu-id="a258e-804">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a258e-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a258e-805">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="a258e-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a258e-806">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a258e-807">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a258e-807">Highlights since the last major release</span></span>
* <span data-ttu-id="a258e-808">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="a258e-808">General availability of `Az` module</span></span>
* <span data-ttu-id="a258e-809">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="a258e-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a258e-810">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="a258e-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a258e-811">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a258e-812">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a258e-813">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a258e-814">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a258e-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-815">Az.Accounts</span></span>
* <span data-ttu-id="a258e-816">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="a258e-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a258e-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a258e-817">Az.Batch</span></span>
* <span data-ttu-id="a258e-818">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a258e-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a258e-819">Az.Cdn</span></span>
* <span data-ttu-id="a258e-820">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a258e-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a258e-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="a258e-822">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-823">Az.Compute</span></span>
* <span data-ttu-id="a258e-824">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="a258e-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a258e-825">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a258e-826">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-827">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-828">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="a258e-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-830">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a258e-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a258e-831">Az.EventGrid</span></span>
* <span data-ttu-id="a258e-832">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a258e-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a258e-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a258e-833">Az.EventHub</span></span>
* <span data-ttu-id="a258e-834">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a258e-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a258e-835">Az.HDInsight</span></span>
* <span data-ttu-id="a258e-836">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a258e-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a258e-837">Az.IotHub</span></span>
* <span data-ttu-id="a258e-838">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a258e-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a258e-839">Az.KeyVault</span></span>
* <span data-ttu-id="a258e-840">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a258e-841">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a258e-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a258e-842">Az.MachineLearning</span></span>
* <span data-ttu-id="a258e-843">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a258e-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a258e-844">Az.Media</span></span>
* <span data-ttu-id="a258e-845">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a258e-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-846">Az.Monitor</span></span>
  * <span data-ttu-id="a258e-847">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="a258e-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a258e-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a258e-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a258e-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a258e-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a258e-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a258e-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a258e-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a258e-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a258e-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a258e-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a258e-853">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-854">Az.Network</span></span>
* <span data-ttu-id="a258e-855">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a258e-856">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a258e-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a258e-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="a258e-858">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="a258e-860">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a258e-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a258e-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a258e-862">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-864">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a258e-865">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a258e-866">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a258e-867">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a258e-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a258e-868">Az.RedisCache</span></span>
* <span data-ttu-id="a258e-869">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-870">Az.Resources</span></span>
* <span data-ttu-id="a258e-871">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-872">Az.Sql</span></span>
* <span data-ttu-id="a258e-873">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="a258e-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a258e-874">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a258e-875">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="a258e-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a258e-876">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="a258e-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a258e-877">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="a258e-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a258e-878">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="a258e-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a258e-879">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-880">Az.Websites</span></span>
* <span data-ttu-id="a258e-881">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="a258e-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a258e-882">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a258e-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a258e-883">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a258e-884">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a258e-885">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a258e-886">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a258e-886">Highlights since the last major release</span></span>
* <span data-ttu-id="a258e-887">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="a258e-887">General availability of `Az` module</span></span>
* <span data-ttu-id="a258e-888">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="a258e-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a258e-889">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="a258e-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a258e-890">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a258e-891">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a258e-892">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a258e-893">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a258e-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-894">Az.Accounts</span></span>
* <span data-ttu-id="a258e-895">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="a258e-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a258e-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a258e-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="a258e-897">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="a258e-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a258e-898">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a258e-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-899">Az.Automation</span></span>
* <span data-ttu-id="a258e-900">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="a258e-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a258e-901">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a258e-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a258e-902">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="a258e-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-903">Az.Compute</span></span>
* <span data-ttu-id="a258e-904">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a258e-905">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="a258e-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a258e-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="a258e-907">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="a258e-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-908">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-909">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a258e-910">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-911">Az.Resources</span></span>
* <span data-ttu-id="a258e-912">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a258e-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a258e-913">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a258e-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a258e-914">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="a258e-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a258e-915">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a258e-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a258e-916">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="a258e-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a258e-917">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a258e-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-918">Az.Sql</span></span>
* <span data-ttu-id="a258e-919">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="a258e-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-920">Az.Storage</span></span>
* <span data-ttu-id="a258e-921">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="a258e-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a258e-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a258e-922">New-AzStorageContext</span></span>
* <span data-ttu-id="a258e-923">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="a258e-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a258e-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a258e-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a258e-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a258e-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a258e-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a258e-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a258e-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a258e-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a258e-928">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="a258e-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a258e-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a258e-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a258e-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a258e-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a258e-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a258e-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a258e-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a258e-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a258e-933">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a258e-934">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a258e-934">Highlights since the last major release</span></span>
* <span data-ttu-id="a258e-935">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="a258e-935">General availability of `Az` module</span></span>
* <span data-ttu-id="a258e-936">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="a258e-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a258e-937">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="a258e-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a258e-938">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a258e-939">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a258e-940">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a258e-941">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-942">Az.Automation</span></span>
* <span data-ttu-id="a258e-943">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="a258e-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a258e-944">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="a258e-944">Dynamic grouping</span></span>
    * <span data-ttu-id="a258e-945">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="a258e-945">Pre-Post script</span></span>
    * <span data-ttu-id="a258e-946">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="a258e-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-947">Az.Compute</span></span>
* <span data-ttu-id="a258e-948">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a258e-949">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a258e-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a258e-950">Az.KeyVault</span></span>
* <span data-ttu-id="a258e-951">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-952">Az.Network</span></span>
* <span data-ttu-id="a258e-953">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a258e-954">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-956">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a258e-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a258e-957">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-958">Az.Resources</span></span>
* <span data-ttu-id="a258e-959">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a258e-960">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a258e-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-961">Az.Sql</span></span>
* <span data-ttu-id="a258e-962">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a258e-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-963">Az.Storage</span></span>
* <span data-ttu-id="a258e-964">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a258e-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a258e-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a258e-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a258e-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a258e-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a258e-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a258e-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a258e-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a258e-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a258e-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a258e-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a258e-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-971">Az.Websites</span></span>
* <span data-ttu-id="a258e-972">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="a258e-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a258e-973">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-974">Az.Accounts</span></span>
* <span data-ttu-id="a258e-975">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a258e-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a258e-976">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-977">Az.Automation</span></span>
* <span data-ttu-id="a258e-978">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="a258e-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a258e-979">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="a258e-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a258e-980">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a258e-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a258e-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a258e-981">Az.Cdn</span></span>
* <span data-ttu-id="a258e-982">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="a258e-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-983">Az.Compute</span></span>
* <span data-ttu-id="a258e-984">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-985">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-986">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a258e-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a258e-987">Az.LogicApp</span></span>
* <span data-ttu-id="a258e-988">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a258e-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-989">Az.Network</span></span>
* <span data-ttu-id="a258e-990">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-992">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="a258e-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a258e-993">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="a258e-993">SDK Update</span></span>
* <span data-ttu-id="a258e-994">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a258e-995">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-996">Az.Resources</span></span>
* <span data-ttu-id="a258e-997">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a258e-998">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a258e-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a258e-999">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a258e-1000">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a258e-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a258e-1001">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a258e-1002">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a258e-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1003">Az.Sql</span></span>
* <span data-ttu-id="a258e-1004">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a258e-1005">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-1006">Az.Storage</span></span>
* <span data-ttu-id="a258e-1007">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a258e-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a258e-1008">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a258e-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="a258e-1010">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-1011">Az.Automation</span></span>
* <span data-ttu-id="a258e-1012">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a258e-1013">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a258e-1014">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a258e-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a258e-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="a258e-1016">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a258e-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1017">Az.Compute</span></span>
* <span data-ttu-id="a258e-1018">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a258e-1019">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a258e-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a258e-1020">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a258e-1021">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="a258e-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-1023">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a258e-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a258e-1024">Az.EventHub</span></span>
* <span data-ttu-id="a258e-1025">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a258e-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a258e-1026">Az.KeyVault</span></span>
* <span data-ttu-id="a258e-1027">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a258e-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a258e-1028">Az.LogicApp</span></span>
* <span data-ttu-id="a258e-1029">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a258e-1030">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a258e-1031">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="a258e-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a258e-1032">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a258e-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a258e-1033">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a258e-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a258e-1034">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a258e-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a258e-1035">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a258e-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a258e-1036">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a258e-1037">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a258e-1038">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a258e-1039">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a258e-1040">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a258e-1041">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a258e-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-1042">Az.Monitor</span></span>
* <span data-ttu-id="a258e-1043">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1044">Az.Network</span></span>
* <span data-ttu-id="a258e-1045">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="a258e-1047">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a258e-1048">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a258e-1049">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="a258e-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a258e-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1050">Az.Resources</span></span>
* <span data-ttu-id="a258e-1051">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a258e-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a258e-1052">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a258e-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a258e-1053">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a258e-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a258e-1054">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="a258e-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1055">Az.Sql</span></span>
* <span data-ttu-id="a258e-1056">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a258e-1057">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="a258e-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1058">Az.Websites</span></span>
* <span data-ttu-id="a258e-1059">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a258e-1060">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-1061">Az.Accounts</span></span>
* <span data-ttu-id="a258e-1062">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="a258e-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a258e-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="a258e-1064">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="a258e-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1065">Az.Compute</span></span>
* <span data-ttu-id="a258e-1066">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a258e-1067">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a258e-1068">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="a258e-1070">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="a258e-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1071">Az.Resources</span></span>
* <span data-ttu-id="a258e-1072">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a258e-1073">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a258e-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a258e-1074">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a258e-1075">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a258e-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1076">Az.Sql</span></span>
* <span data-ttu-id="a258e-1077">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a258e-1078">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="a258e-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a258e-1079">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a258e-1080">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-1081">Az.Accounts</span></span>
* <span data-ttu-id="a258e-1082">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a258e-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a258e-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="a258e-1084">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="a258e-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="a258e-1086">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="a258e-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a258e-1087">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-1088">Az.Accounts</span></span>
* <span data-ttu-id="a258e-1089">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a258e-1090">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a258e-1091">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a258e-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a258e-1092">Az.Aks</span></span>
* <span data-ttu-id="a258e-1093">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a258e-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-1094">Az.Automation</span></span>
* <span data-ttu-id="a258e-1095">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a258e-1096">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a258e-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a258e-1097">Az.Cdn</span></span>
* <span data-ttu-id="a258e-1098">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1099">Az.Compute</span></span>
* <span data-ttu-id="a258e-1100">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a258e-1101">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a258e-1102">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a258e-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a258e-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a258e-1104">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a258e-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a258e-1105">Az.DataFactory</span></span>
* <span data-ttu-id="a258e-1106">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-1108">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a258e-1109">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a258e-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a258e-1110">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a258e-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a258e-1111">Az.IotHub</span></span>
* <span data-ttu-id="a258e-1112">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a258e-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a258e-1113">Az.KeyVault</span></span>
* <span data-ttu-id="a258e-1114">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1115">Az.Network</span></span>
* <span data-ttu-id="a258e-1116">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1117">Az.Resources</span></span>
* <span data-ttu-id="a258e-1118">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a258e-1119">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="a258e-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a258e-1120">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="a258e-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a258e-1121">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a258e-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a258e-1122">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a258e-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a258e-1123">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a258e-1124">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a258e-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a258e-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-1126">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a258e-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a258e-1127">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1127">Fix some error messages.</span></span>
* <span data-ttu-id="a258e-1128">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="a258e-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a258e-1129">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="a258e-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a258e-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a258e-1130">Az.SignalR</span></span>
* <span data-ttu-id="a258e-1131">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1132">Az.Sql</span></span>
* <span data-ttu-id="a258e-1133">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a258e-1134">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a258e-1135">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="a258e-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a258e-1136">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="a258e-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-1137">Az.Storage</span></span>
* <span data-ttu-id="a258e-1138">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a258e-1139">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a258e-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a258e-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a258e-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a258e-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a258e-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a258e-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a258e-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="a258e-1143">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1144">Az.Websites</span></span>
* <span data-ttu-id="a258e-1145">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a258e-1146">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="a258e-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a258e-1147">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a258e-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a258e-1148">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="a258e-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a258e-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-1149">Az.Accounts</span></span>
* <span data-ttu-id="a258e-1150">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1151">Az.Compute</span></span>
* <span data-ttu-id="a258e-1152">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="a258e-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a258e-1153">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a258e-1154">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-1156">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="a258e-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a258e-1157">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a258e-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a258e-1158">Az.EventGrid</span></span>
* <span data-ttu-id="a258e-1159">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a258e-1160">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a258e-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a258e-1161">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a258e-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a258e-1162">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="a258e-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a258e-1163">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a258e-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a258e-1164">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a258e-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a258e-1165">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a258e-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a258e-1166">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="a258e-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a258e-1167">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a258e-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a258e-1168">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a258e-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="a258e-1169">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a258e-1170">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="a258e-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a258e-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a258e-1171">Az.IotHub</span></span>
* <span data-ttu-id="a258e-1172">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a258e-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a258e-1173">Az.LogicApp</span></span>
* <span data-ttu-id="a258e-1174">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="a258e-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1175">Az.Resources</span></span>
* <span data-ttu-id="a258e-1176">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a258e-1177">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a258e-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a258e-1178">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a258e-1179">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a258e-1180">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="a258e-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a258e-1181">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a258e-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a258e-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a258e-1182">Az.SignalR</span></span>
* <span data-ttu-id="a258e-1183">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1184">Az.Sql</span></span>
* <span data-ttu-id="a258e-1185">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a258e-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-1186">Az.Storage</span></span>
* <span data-ttu-id="a258e-1187">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a258e-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a258e-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="a258e-1189">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="a258e-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a258e-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a258e-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1191">Az.Websites</span></span>
* <span data-ttu-id="a258e-1192">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a258e-1193">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a258e-1194">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a258e-1195">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a258e-1195">General</span></span>

- <span data-ttu-id="a258e-1196">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="a258e-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="a258e-1197">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="a258e-1197">Online help for each module</span></span>
- <span data-ttu-id="a258e-1198">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="a258e-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a258e-1199">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a258e-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a258e-1200">Az.Accounts</span></span>
- <span data-ttu-id="a258e-1201">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a258e-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="a258e-1202">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="a258e-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a258e-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a258e-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="a258e-1204">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="a258e-1204">Fixes for #7002</span></span>
- <span data-ttu-id="a258e-1205">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a258e-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a258e-1206">Az.Batch</span></span>
- <span data-ttu-id="a258e-1207">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a258e-1208">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="a258e-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a258e-1209">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a258e-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a258e-1210">Az.Billing</span></span>
- <span data-ttu-id="a258e-1211">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a258e-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="a258e-1213">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a258e-1214">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a258e-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="a258e-1216">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a258e-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a258e-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a258e-1218">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="a258e-1220">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a258e-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a258e-1221">Az.Monitor</span></span>
- <span data-ttu-id="a258e-1222">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a258e-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a258e-1223">Az.KeyVault</span></span>
- <span data-ttu-id="a258e-1224">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a258e-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a258e-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="a258e-1226">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="a258e-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a258e-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a258e-1227">Az.Media</span></span>
- <span data-ttu-id="a258e-1228">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="a258e-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a258e-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1229">Az.Network</span></span>
<span data-ttu-id="a258e-1230">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a258e-1231">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a258e-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="a258e-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a258e-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a258e-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a258e-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a258e-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a258e-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a258e-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a258e-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a258e-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a258e-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a258e-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a258e-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a258e-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a258e-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a258e-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a258e-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a258e-1240">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a258e-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a258e-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a258e-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a258e-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a258e-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a258e-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a258e-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a258e-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a258e-1246">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a258e-1247">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a258e-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a258e-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a258e-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a258e-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a258e-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a258e-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a258e-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a258e-1251">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a258e-1252">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a258e-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="a258e-1254">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a258e-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a258e-1255">Az.Profile</span></span>
- <span data-ttu-id="a258e-1256">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="a258e-1258">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a258e-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1259">Az.Resources</span></span>
- <span data-ttu-id="a258e-1260">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a258e-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="a258e-1262">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="a258e-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a258e-1263">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a258e-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a258e-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="a258e-1265">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a258e-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a258e-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1266">Az.Sql</span></span>
- <span data-ttu-id="a258e-1267">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a258e-1268">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a258e-1269">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a258e-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-1270">Az.Storage</span></span>
- <span data-ttu-id="a258e-1271">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a258e-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1272">Az.Websites</span></span>
- <span data-ttu-id="a258e-1273">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a258e-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a258e-1274">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a258e-1275">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a258e-1275">General</span></span>

* <span data-ttu-id="a258e-1276">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="a258e-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a258e-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1277">Az.Compute</span></span>

* <span data-ttu-id="a258e-1278">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="a258e-1280">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a258e-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a258e-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="a258e-1282">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="a258e-1283">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a258e-1284">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a258e-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="a258e-1286">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a258e-1287">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="a258e-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a258e-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1288">Az.Resources</span></span>

* <span data-ttu-id="a258e-1289">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a258e-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a258e-1290">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a258e-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a258e-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1291">Az.Sql</span></span>

* <span data-ttu-id="a258e-1292">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="a258e-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a258e-1293">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a258e-1294">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a258e-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-1295">Az.Storage</span></span>

* <span data-ttu-id="a258e-1296">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a258e-1297">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a258e-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a258e-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a258e-1299">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="a258e-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a258e-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a258e-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a258e-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a258e-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1302">Az.Websites</span></span>

* <span data-ttu-id="a258e-1303">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a258e-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a258e-1304">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a258e-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a258e-1305">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="a258e-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a258e-1306">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a258e-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a258e-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="a258e-1308">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a258e-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a258e-1309">Az.Automation</span></span>
* <span data-ttu-id="a258e-1310">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a258e-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a258e-1311">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a258e-1312">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a258e-1313">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a258e-1314">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a258e-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1315">Az.Compute</span></span>
* <span data-ttu-id="a258e-1316">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a258e-1317">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a258e-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="a258e-1319">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a258e-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a258e-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a258e-1321">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a258e-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1322">Az.Network</span></span>
* <span data-ttu-id="a258e-1323">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a258e-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a258e-1324">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a258e-1325">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a258e-1326">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a258e-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a258e-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a258e-1328">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a258e-1329">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="a258e-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a258e-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a258e-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a258e-1331">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="a258e-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a258e-1332">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a258e-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a258e-1333">Az.Relay</span></span>
* <span data-ttu-id="a258e-1334">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="a258e-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a258e-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1335">Az.Resources</span></span>
* <span data-ttu-id="a258e-1336">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a258e-1337">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="a258e-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a258e-1338">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a258e-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a258e-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-1340">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a258e-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1341">Az.Sql</span></span>
* <span data-ttu-id="a258e-1342">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a258e-1343">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a258e-1344">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a258e-1345">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a258e-1346">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a258e-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a258e-1347">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a258e-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a258e-1348">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a258e-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a258e-1349">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a258e-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a258e-1350">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a258e-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a258e-1351">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="a258e-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a258e-1352">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a258e-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a258e-1353">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="a258e-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a258e-1354">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="a258e-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a258e-1355">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="a258e-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a258e-1356">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a258e-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a258e-1357">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a258e-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a258e-1358">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a258e-1359">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a258e-1360">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a258e-1360">General</span></span>
* <span data-ttu-id="a258e-1361">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="a258e-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a258e-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a258e-1362">Az.Profile</span></span>
* <span data-ttu-id="a258e-1363">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a258e-1364">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a258e-1365">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a258e-1366">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a258e-1367">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a258e-1368">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a258e-1369">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="a258e-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a258e-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="a258e-1371">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1372">Az.Compute</span></span>
* <span data-ttu-id="a258e-1373">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a258e-1374">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="a258e-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a258e-1375">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="a258e-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-1377">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="a258e-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a258e-1378">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a258e-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a258e-1379">Az.Insights</span></span>
* <span data-ttu-id="a258e-1380">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="a258e-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a258e-1381">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="a258e-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a258e-1382">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="a258e-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a258e-1383">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1384">Az.Network</span></span>
* <span data-ttu-id="a258e-1385">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a258e-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a258e-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a258e-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a258e-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a258e-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a258e-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a258e-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a258e-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a258e-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a258e-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a258e-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a258e-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a258e-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a258e-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a258e-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="a258e-1393">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1394">Az.Resources</span></span>
* <span data-ttu-id="a258e-1395">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a258e-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a258e-1396">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="a258e-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a258e-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a258e-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="a258e-1398">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="a258e-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a258e-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a258e-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="a258e-1400">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a258e-1401">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a258e-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a258e-1402">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="a258e-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a258e-1403">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="a258e-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a258e-1404">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a258e-1405">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a258e-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a258e-1406">Az.Profile</span></span>
* <span data-ttu-id="a258e-1407">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a258e-1408">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1409">Az.Compute</span></span>
* <span data-ttu-id="a258e-1410">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="a258e-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a258e-1411">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a258e-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a258e-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="a258e-1413">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a258e-1414">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a258e-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a258e-1415">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="a258e-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a258e-1416">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="a258e-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a258e-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a258e-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1418">Az.Network</span></span>
* <span data-ttu-id="a258e-1419">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="a258e-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a258e-1420">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1421">Az.Resources</span></span>
* <span data-ttu-id="a258e-1422">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a258e-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a258e-1423">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a258e-1424">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a258e-1425">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a258e-1425">Azure.Storage</span></span>
* <span data-ttu-id="a258e-1426">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="a258e-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a258e-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a258e-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a258e-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a258e-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a258e-1429">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="a258e-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a258e-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a258e-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a258e-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a258e-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="a258e-1432">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a258e-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a258e-1433">Az.Compute</span></span>
* <span data-ttu-id="a258e-1434">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="a258e-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a258e-1435">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a258e-1436">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="a258e-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a258e-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a258e-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a258e-1438">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a258e-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a258e-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a258e-1439">Az.Network</span></span>
* <span data-ttu-id="a258e-1440">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a258e-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a258e-1441">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1441">new cmdlets added</span></span>
    - <span data-ttu-id="a258e-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a258e-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a258e-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a258e-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a258e-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a258e-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a258e-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a258e-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a258e-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a258e-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a258e-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a258e-1448">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a258e-1449">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a258e-1450">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a258e-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a258e-1451">Az.RedisCache</span></span>
* <span data-ttu-id="a258e-1452">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="a258e-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a258e-1453">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a258e-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a258e-1454">Az.Resources</span></span>
* <span data-ttu-id="a258e-1455">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a258e-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a258e-1456">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="a258e-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a258e-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a258e-1457">Az.Sql</span></span>
* <span data-ttu-id="a258e-1458">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="a258e-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a258e-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a258e-1459">Az.Websites</span></span>
* <span data-ttu-id="a258e-1460">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="a258e-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a258e-1461">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="a258e-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a258e-1462">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="a258e-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a258e-1463">Erste Version</span><span class="sxs-lookup"><span data-stu-id="a258e-1463">Initial Release</span></span>