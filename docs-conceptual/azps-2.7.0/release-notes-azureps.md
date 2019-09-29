---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226438"
---
## <a name="270---september-2019"></a><span data-ttu-id="2ea4d-101">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2ea4d-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ea4d-102">Az.ApiManagement</span></span>
* <span data-ttu-id="2ea4d-103">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2ea4d-104">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2ea4d-105">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-106">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-107">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2ea4d-108">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2ea4d-109">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-110">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-111">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2ea4d-112">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2ea4d-113">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2ea4d-114">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2ea4d-115">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2ea4d-116">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2ea4d-117">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2ea4d-118">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2ea4d-119">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-120">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-121">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2ea4d-122">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2ea4d-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2ea4d-123">Az.HDInsight</span></span>
* <span data-ttu-id="2ea4d-124">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2ea4d-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-125">Az.IotHub</span></span>
* <span data-ttu-id="2ea4d-126">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2ea4d-127">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2ea4d-128">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-128">New cmdlets are:</span></span>
    - <span data-ttu-id="2ea4d-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2ea4d-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2ea4d-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2ea4d-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2ea4d-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2ea4d-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2ea4d-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2ea4d-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2ea4d-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-133">Az.Monitor</span></span>
* <span data-ttu-id="2ea4d-134">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="2ea4d-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2ea4d-135">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2ea4d-136">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2ea4d-137">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2ea4d-138">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2ea4d-139">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2ea4d-140">Derzeit ist der Wert auf „false“ festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2ea4d-141">\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2ea4d-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2ea4d-142">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2ea4d-143">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2ea4d-144">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2ea4d-145">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2ea4d-146">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="2ea4d-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2ea4d-147">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2ea4d-148">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2ea4d-149">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2ea4d-150">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2ea4d-151">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2ea4d-152">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2ea4d-153">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-153">Overall improved help files</span></span>
* <span data-ttu-id="2ea4d-154">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-155">Az.Network</span></span>
* <span data-ttu-id="2ea4d-156">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="2ea4d-157">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2ea4d-158">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2ea4d-159">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2ea4d-160">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2ea4d-161">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2ea4d-162">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2ea4d-163">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2ea4d-164">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2ea4d-165">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2ea4d-166">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2ea4d-167">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="2ea4d-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2ea4d-168">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-168">New cmdlets</span></span>
        - <span data-ttu-id="2ea4d-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2ea4d-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2ea4d-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2ea4d-171">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="2ea4d-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2ea4d-172">New-VpnSite</span></span>
        - <span data-ttu-id="2ea4d-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2ea4d-173">Update-VpnSite</span></span>
        - <span data-ttu-id="2ea4d-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-174">New-VpnConnection</span></span>
        - <span data-ttu-id="2ea4d-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-175">Update-VpnConnection</span></span>
* <span data-ttu-id="2ea4d-176">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-178">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2ea4d-179">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-180">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-181">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="2ea4d-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-183">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2ea4d-184">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2ea4d-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2ea4d-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2ea4d-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2ea4d-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2ea4d-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2ea4d-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2ea4d-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2ea4d-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2ea4d-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2ea4d-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2ea4d-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2ea4d-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2ea4d-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2ea4d-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2ea4d-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2ea4d-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2ea4d-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2ea4d-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2ea4d-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2ea4d-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2ea4d-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2ea4d-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2ea4d-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="2ea4d-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2ea4d-198">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2ea4d-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2ea4d-199">Az.SignalR</span></span>
* <span data-ttu-id="2ea4d-200">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-201">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-202">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2ea4d-203">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2ea4d-204">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="2ea4d-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2ea4d-205">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2ea4d-206">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-207">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-208">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2ea4d-209">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2ea4d-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2ea4d-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2ea4d-212">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2ea4d-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2ea4d-214">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="2ea4d-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2ea4d-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ea4d-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2ea4d-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ea4d-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2ea4d-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ea4d-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2ea4d-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ea4d-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-219">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-220">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2ea4d-221">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2ea4d-222">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2ea4d-223">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2ea4d-224">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2ea4d-224">General</span></span>
* <span data-ttu-id="2ea4d-225">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-226">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-227">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2ea4d-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2ea4d-228">Az.Aks</span></span>
* <span data-ttu-id="2ea4d-229">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2ea4d-230">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="2ea4d-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2ea4d-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ea4d-231">Az.ApiManagement</span></span>
* <span data-ttu-id="2ea4d-232">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="2ea4d-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2ea4d-233">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2ea4d-234">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2ea4d-235">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="2ea4d-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2ea4d-236">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2ea4d-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2ea4d-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2ea4d-237">Az.Batch</span></span>
* <span data-ttu-id="2ea4d-238">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2ea4d-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2ea4d-239">Az.Cdn</span></span>
* <span data-ttu-id="2ea4d-240">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-241">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-242">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2ea4d-243">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2ea4d-244">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2ea4d-245">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2ea4d-246">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2ea4d-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2ea4d-247">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2ea4d-248">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2ea4d-249">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-250">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-251">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2ea4d-252">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2ea4d-253">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2ea4d-254">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-256">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2ea4d-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-257">Az.EventHub</span></span>
* <span data-ttu-id="2ea4d-258">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2ea4d-259">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2ea4d-260">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2ea4d-261">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2ea4d-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2ea4d-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2ea4d-263">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2ea4d-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-264">Az.Monitor</span></span>
* <span data-ttu-id="2ea4d-265">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-266">Az.Network</span></span>
* <span data-ttu-id="2ea4d-267">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2ea4d-268">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="2ea4d-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2ea4d-269">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="2ea4d-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2ea4d-270">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2ea4d-271">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="2ea4d-272">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2ea4d-273">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="2ea4d-275">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2ea4d-276">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-276">Added example</span></span>
    - <span data-ttu-id="2ea4d-277">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2ea4d-278">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2ea4d-279">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-281">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-282">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-283">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2ea4d-284">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2ea4d-285">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2ea4d-286">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2ea4d-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-287">Az.ServiceBus</span></span>
* <span data-ttu-id="2ea4d-288">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2ea4d-289">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2ea4d-290">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-292">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2ea4d-293">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2ea4d-294">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="2ea4d-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2ea4d-295">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="2ea4d-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2ea4d-296">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="2ea4d-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2ea4d-297">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-298">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-299">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-300">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-301">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2ea4d-302">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="2ea4d-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2ea4d-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2ea4d-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2ea4d-305">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="2ea4d-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2ea4d-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-307">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-308">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2ea4d-309">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-310">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-311">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2ea4d-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2ea4d-313">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-314">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-315">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="2ea4d-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="2ea4d-317">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-318">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-319">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2ea4d-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2ea4d-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2ea4d-321">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2ea4d-322">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-323">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-324">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2ea4d-325">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2ea4d-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-326">Az.EventHub</span></span>
* <span data-ttu-id="2ea4d-327">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2ea4d-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2ea4d-328">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2ea4d-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2ea4d-329">Az.KeyVault</span></span>
* <span data-ttu-id="2ea4d-330">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2ea4d-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2ea4d-331">Az.LogicApp</span></span>
* <span data-ttu-id="2ea4d-332">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2ea4d-333">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2ea4d-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-334">Az.ManagedServices</span></span>
* <span data-ttu-id="2ea4d-335">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-336">Az.Network</span></span>
* <span data-ttu-id="2ea4d-337">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2ea4d-338">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-338">New cmdlets</span></span>
        - <span data-ttu-id="2ea4d-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea4d-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2ea4d-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2ea4d-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2ea4d-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2ea4d-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2ea4d-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2ea4d-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="2ea4d-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2ea4d-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2ea4d-347">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ea4d-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2ea4d-348">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2ea4d-349">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2ea4d-350">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2ea4d-351">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2ea4d-352">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2ea4d-353">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-353">Updated cmdlets</span></span>
        - <span data-ttu-id="2ea4d-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2ea4d-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2ea4d-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2ea4d-357">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2ea4d-358">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2ea4d-359">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="2ea4d-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2ea4d-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2ea4d-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2ea4d-363">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2ea4d-364">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2ea4d-365">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="2ea4d-367">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="2ea4d-368">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-370">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2ea4d-371">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2ea4d-372">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2ea4d-373">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2ea4d-374">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2ea4d-375">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2ea4d-376">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2ea4d-377">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2ea4d-378">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2ea4d-379">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-380">Az.Resources</span></span>
- <span data-ttu-id="2ea4d-381">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2ea4d-382">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2ea4d-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-383">Az.ServiceBus</span></span>
* <span data-ttu-id="2ea4d-384">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2ea4d-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2ea4d-385">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-386">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-387">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2ea4d-388">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2ea4d-389">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-390">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-391">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2ea4d-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2ea4d-392">Az.StorageSync</span></span>
* <span data-ttu-id="2ea4d-393">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2ea4d-394">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-395">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-396">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2ea4d-397">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2ea4d-398">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2ea4d-399">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-400">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-401">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2ea4d-402">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2ea4d-403">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="2ea4d-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2ea4d-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-404">Az.Advisor</span></span>
* <span data-ttu-id="2ea4d-405">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2ea4d-406">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2ea4d-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ea4d-407">Az.ApiManagement</span></span>
* <span data-ttu-id="2ea4d-408">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2ea4d-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2ea4d-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2ea4d-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2ea4d-410">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2ea4d-411">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2ea4d-412">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2ea4d-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2ea4d-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2ea4d-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2ea4d-414">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-415">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-416">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-417">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-418">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-419">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-420">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2ea4d-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2ea4d-421">Az.EventGrid</span></span>
* <span data-ttu-id="2ea4d-422">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2ea4d-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-423">Az.IotHub</span></span>
* <span data-ttu-id="2ea4d-424">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-425">Az.Network</span></span>
* <span data-ttu-id="2ea4d-426">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2ea4d-427">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2ea4d-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="2ea4d-429">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2ea4d-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2ea4d-430">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2ea4d-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="2ea4d-432">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-434">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="2ea4d-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-435">Az.Resources</span></span>
    - <span data-ttu-id="2ea4d-436">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2ea4d-437">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2ea4d-438">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2ea4d-439">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2ea4d-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-440">Az.ServiceBus</span></span>
* <span data-ttu-id="2ea4d-441">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="2ea4d-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-442">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-443">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2ea4d-444">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2ea4d-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2ea4d-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2ea4d-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2ea4d-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2ea4d-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2ea4d-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2ea4d-451">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-452">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-453">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2ea4d-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2ea4d-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2ea4d-455">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2ea4d-456">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2ea4d-457">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="2ea4d-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2ea4d-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2ea4d-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2ea4d-460">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="2ea4d-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2ea4d-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2ea4d-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2ea4d-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2ea4d-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2ea4d-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2ea4d-463">Az.StorageSync</span></span>
* <span data-ttu-id="2ea4d-464">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2ea4d-465">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-466">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-467">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="2ea4d-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2ea4d-468">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2ea4d-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2ea4d-469">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2ea4d-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2ea4d-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2ea4d-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2ea4d-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-472">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-473">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2ea4d-474">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2ea4d-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2ea4d-475">Az.Dns</span></span>
* <span data-ttu-id="2ea4d-476">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2ea4d-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2ea4d-477">Az.EventGrid</span></span>
* <span data-ttu-id="2ea4d-478">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2ea4d-479">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-479">New cmdlets:</span></span>
    - <span data-ttu-id="2ea4d-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2ea4d-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2ea4d-481">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2ea4d-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2ea4d-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2ea4d-483">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2ea4d-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2ea4d-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2ea4d-485">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2ea4d-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2ea4d-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2ea4d-487">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2ea4d-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2ea4d-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2ea4d-489">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2ea4d-490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2ea4d-491">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2ea4d-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2ea4d-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2ea4d-493">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="2ea4d-494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2ea4d-495">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2ea4d-496">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="2ea4d-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2ea4d-498">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2ea4d-499">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2ea4d-500">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2ea4d-501">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2ea4d-502">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="2ea4d-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2ea4d-503">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="2ea4d-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2ea4d-504">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2ea4d-505">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="2ea4d-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2ea4d-507">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2ea4d-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2ea4d-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2ea4d-509">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2ea4d-510">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2ea4d-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-511">Az.FrontDoor</span></span>
* <span data-ttu-id="2ea4d-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2ea4d-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2ea4d-513">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2ea4d-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2ea4d-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2ea4d-515">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-516">Az.Network</span></span>
* <span data-ttu-id="2ea4d-517">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2ea4d-518">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-518">New cmdlets</span></span>
        - <span data-ttu-id="2ea4d-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2ea4d-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2ea4d-520">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2ea4d-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2ea4d-521">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-521">New cmdlets</span></span> 
        - <span data-ttu-id="2ea4d-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2ea4d-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2ea4d-523">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2ea4d-524">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-524">New cmdlets</span></span> 
        - <span data-ttu-id="2ea4d-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="2ea4d-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2ea4d-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2ea4d-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2ea4d-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2ea4d-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2ea4d-530">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2ea4d-531">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-531">New cmdlets</span></span>
        - <span data-ttu-id="2ea4d-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea4d-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2ea4d-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea4d-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2ea4d-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea4d-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2ea4d-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2ea4d-536">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2ea4d-537">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="2ea4d-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2ea4d-538">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="2ea4d-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2ea4d-539">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2ea4d-540">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2ea4d-541">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2ea4d-542">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2ea4d-543">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="2ea4d-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2ea4d-544">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2ea4d-545">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2ea4d-546">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2ea4d-547">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2ea4d-548">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2ea4d-549">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2ea4d-550">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2ea4d-551">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2ea4d-552">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2ea4d-553">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2ea4d-554">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="2ea4d-555">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="2ea4d-556">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2ea4d-557">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2ea4d-558">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="2ea4d-560">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="2ea4d-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-561">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-562">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2ea4d-563">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2ea4d-564">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2ea4d-565">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-567">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-568">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-569">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2ea4d-570">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2ea4d-571">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2ea4d-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2ea4d-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2ea4d-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2ea4d-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2ea4d-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2ea4d-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2ea4d-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2ea4d-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2ea4d-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2ea4d-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-577">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-578">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="2ea4d-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2ea4d-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="2ea4d-580">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="2ea4d-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2ea4d-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-582">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-583">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2ea4d-584">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2ea4d-585">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2ea4d-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2ea4d-586">Az.Cdn</span></span>
* <span data-ttu-id="2ea4d-587">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-588">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-589">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2ea4d-590">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2ea4d-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2ea4d-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-591">Az.EventHub</span></span>
* <span data-ttu-id="2ea4d-592">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="2ea4d-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2ea4d-593">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="2ea4d-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-594">Az.Network</span></span>
* <span data-ttu-id="2ea4d-595">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2ea4d-596">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2ea4d-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="2ea4d-598">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-600">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2ea4d-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-601">Az.ServiceBus</span></span>
* <span data-ttu-id="2ea4d-602">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="2ea4d-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-604">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2ea4d-605">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-606">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-607">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2ea4d-608">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2ea4d-609">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2ea4d-610">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="2ea4d-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-611">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-612">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2ea4d-613">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2ea4d-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ea4d-614">Az.ApiManagement</span></span>
* <span data-ttu-id="2ea4d-615">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2ea4d-616">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="2ea4d-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2ea4d-617">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2ea4d-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2ea4d-618">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="2ea4d-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2ea4d-619">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="2ea4d-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2ea4d-620">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="2ea4d-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2ea4d-621">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2ea4d-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2ea4d-622">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2ea4d-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2ea4d-623">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2ea4d-624">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="2ea4d-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2ea4d-625">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="2ea4d-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2ea4d-626">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="2ea4d-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2ea4d-627">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="2ea4d-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2ea4d-628">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2ea4d-629">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="2ea4d-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2ea4d-630">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="2ea4d-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2ea4d-631">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="2ea4d-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2ea4d-632">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="2ea4d-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2ea4d-633">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="2ea4d-634">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="2ea4d-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2ea4d-635">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2ea4d-636">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="2ea4d-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2ea4d-637">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2ea4d-638">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="2ea4d-639">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2ea4d-640">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2ea4d-641">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2ea4d-642">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2ea4d-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2ea4d-643">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2ea4d-644">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2ea4d-645">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="2ea4d-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2ea4d-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2ea4d-647">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2ea4d-648">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2ea4d-649">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2ea4d-650">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="2ea4d-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2ea4d-651">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="2ea4d-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2ea4d-652">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2ea4d-653">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2ea4d-654">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="2ea4d-655">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="2ea4d-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2ea4d-656">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2ea4d-657">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2ea4d-658">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2ea4d-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2ea4d-659">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2ea4d-660">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="2ea4d-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2ea4d-661">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="2ea4d-662">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2ea4d-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2ea4d-663">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2ea4d-664">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2ea4d-665">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="2ea4d-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2ea4d-666">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2ea4d-667">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="2ea4d-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2ea4d-668">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2ea4d-669">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2ea4d-670">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2ea4d-671">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2ea4d-672">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2ea4d-673">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2ea4d-674">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2ea4d-675">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2ea4d-676">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2ea4d-677">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2ea4d-678">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2ea4d-679">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="2ea4d-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2ea4d-680">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2ea4d-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2ea4d-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2ea4d-682">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2ea4d-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2ea4d-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2ea4d-684">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2ea4d-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2ea4d-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2ea4d-686">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2ea4d-687">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2ea4d-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2ea4d-689">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="2ea4d-690">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2ea4d-691">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="2ea4d-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-692">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-693">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2ea4d-694">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2ea4d-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2ea4d-695">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2ea4d-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2ea4d-696">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2ea4d-697">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2ea4d-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2ea4d-698">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2ea4d-699">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-700">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-701">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2ea4d-702">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-704">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2ea4d-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-705">Az.Monitor</span></span>
* <span data-ttu-id="2ea4d-706">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-707">Az.Network</span></span>
* <span data-ttu-id="2ea4d-708">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2ea4d-709">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="2ea4d-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2ea4d-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2ea4d-711">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2ea4d-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-712">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-713">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-714">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-715">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="2ea4d-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2ea4d-716">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-717">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-718">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2ea4d-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="2ea4d-720">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="2ea4d-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2ea4d-721">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="2ea4d-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-722">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-723">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2ea4d-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2ea4d-724">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2ea4d-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2ea4d-725">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2ea4d-726">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2ea4d-727">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2ea4d-728">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="2ea4d-729">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-729">Breaking changes</span></span>
    - <span data-ttu-id="2ea4d-730">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2ea4d-731">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2ea4d-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2ea4d-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="2ea4d-733">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2ea4d-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2ea4d-734">Az.Dns</span></span>
* <span data-ttu-id="2ea4d-735">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="2ea4d-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2ea4d-736">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2ea4d-737">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2ea4d-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-738">Az.FrontDoor</span></span>
* <span data-ttu-id="2ea4d-739">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2ea4d-740">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2ea4d-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2ea4d-741">Az.HDInsight</span></span>
* <span data-ttu-id="2ea4d-742">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2ea4d-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2ea4d-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2ea4d-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2ea4d-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2ea4d-745">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2ea4d-746">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2ea4d-747">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2ea4d-748">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2ea4d-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-749">Az.Monitor</span></span>
* <span data-ttu-id="2ea4d-750">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="2ea4d-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2ea4d-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2ea4d-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2ea4d-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2ea4d-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2ea4d-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2ea4d-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2ea4d-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2ea4d-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2ea4d-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2ea4d-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2ea4d-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2ea4d-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2ea4d-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2ea4d-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2ea4d-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2ea4d-762">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="2ea4d-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2ea4d-763">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-764">Az.Network</span></span>
* <span data-ttu-id="2ea4d-765">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2ea4d-766">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-766">New cmdlets</span></span>
        - <span data-ttu-id="2ea4d-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2ea4d-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="2ea4d-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2ea4d-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2ea4d-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2ea4d-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2ea4d-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2ea4d-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2ea4d-771">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-771">Updated cmdlets</span></span>
        - <span data-ttu-id="2ea4d-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2ea4d-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2ea4d-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2ea4d-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2ea4d-774">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2ea4d-775">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2ea4d-776">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2ea4d-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="2ea4d-778">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="2ea4d-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2ea4d-779">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2ea4d-780">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-782">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="2ea4d-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2ea4d-783">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="2ea4d-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2ea4d-784">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="2ea4d-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2ea4d-785">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="2ea4d-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2ea4d-786">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="2ea4d-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2ea4d-787">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2ea4d-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2ea4d-788">Az.Relay</span></span>
* <span data-ttu-id="2ea4d-789">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2ea4d-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-790">Az.ServiceBus</span></span>
* <span data-ttu-id="2ea4d-791">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-792">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-793">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2ea4d-794">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2ea4d-795">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2ea4d-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="2ea4d-797">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2ea4d-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2ea4d-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2ea4d-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-801">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-802">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2ea4d-803">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2ea4d-804">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2ea4d-805">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="2ea4d-805">Highlights since the last major release</span></span>
* <span data-ttu-id="2ea4d-806">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="2ea4d-806">General availability of `Az` module</span></span>
* <span data-ttu-id="2ea4d-807">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2ea4d-808">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2ea4d-809">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2ea4d-810">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2ea4d-811">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2ea4d-812">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-813">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-814">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2ea4d-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2ea4d-815">Az.Batch</span></span>
* <span data-ttu-id="2ea4d-816">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2ea4d-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2ea4d-817">Az.Cdn</span></span>
* <span data-ttu-id="2ea4d-818">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2ea4d-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="2ea4d-820">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-821">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-822">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2ea4d-823">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2ea4d-824">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-825">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-826">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="2ea4d-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-828">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2ea4d-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2ea4d-829">Az.EventGrid</span></span>
* <span data-ttu-id="2ea4d-830">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2ea4d-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-831">Az.EventHub</span></span>
* <span data-ttu-id="2ea4d-832">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="2ea4d-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2ea4d-833">Az.HDInsight</span></span>
* <span data-ttu-id="2ea4d-834">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2ea4d-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-835">Az.IotHub</span></span>
* <span data-ttu-id="2ea4d-836">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2ea4d-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2ea4d-837">Az.KeyVault</span></span>
* <span data-ttu-id="2ea4d-838">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2ea4d-839">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2ea4d-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2ea4d-840">Az.MachineLearning</span></span>
* <span data-ttu-id="2ea4d-841">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2ea4d-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2ea4d-842">Az.Media</span></span>
* <span data-ttu-id="2ea4d-843">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2ea4d-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-844">Az.Monitor</span></span>
  * <span data-ttu-id="2ea4d-845">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2ea4d-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2ea4d-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2ea4d-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2ea4d-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2ea4d-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2ea4d-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2ea4d-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2ea4d-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2ea4d-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2ea4d-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2ea4d-851">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-852">Az.Network</span></span>
* <span data-ttu-id="2ea4d-853">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2ea4d-854">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2ea4d-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2ea4d-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="2ea4d-856">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="2ea4d-858">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2ea4d-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2ea4d-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2ea4d-860">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-862">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2ea4d-863">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2ea4d-864">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2ea4d-865">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2ea4d-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2ea4d-866">Az.RedisCache</span></span>
* <span data-ttu-id="2ea4d-867">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-868">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-869">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-870">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-871">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2ea4d-872">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2ea4d-873">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2ea4d-874">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2ea4d-875">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="2ea4d-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2ea4d-876">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="2ea4d-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2ea4d-877">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-878">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-879">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2ea4d-880">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2ea4d-881">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2ea4d-882">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2ea4d-883">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2ea4d-884">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="2ea4d-884">Highlights since the last major release</span></span>
* <span data-ttu-id="2ea4d-885">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="2ea4d-885">General availability of `Az` module</span></span>
* <span data-ttu-id="2ea4d-886">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2ea4d-887">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2ea4d-888">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2ea4d-889">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2ea4d-890">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2ea4d-891">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-892">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-893">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="2ea4d-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2ea4d-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="2ea4d-895">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2ea4d-896">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-897">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-898">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2ea4d-899">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2ea4d-900">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="2ea4d-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-901">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-902">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2ea4d-903">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="2ea4d-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="2ea4d-905">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="2ea4d-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-906">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-907">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2ea4d-908">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-909">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-910">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2ea4d-911">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2ea4d-912">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="2ea4d-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2ea4d-913">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2ea4d-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2ea4d-914">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2ea4d-915">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2ea4d-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-916">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-917">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-918">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-919">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="2ea4d-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2ea4d-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ea4d-920">New-AzStorageContext</span></span>
* <span data-ttu-id="2ea4d-921">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="2ea4d-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2ea4d-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2ea4d-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2ea4d-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2ea4d-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2ea4d-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2ea4d-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2ea4d-926">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="2ea4d-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2ea4d-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2ea4d-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2ea4d-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2ea4d-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2ea4d-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2ea4d-931">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2ea4d-932">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="2ea4d-932">Highlights since the last major release</span></span>
* <span data-ttu-id="2ea4d-933">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="2ea4d-933">General availability of `Az` module</span></span>
* <span data-ttu-id="2ea4d-934">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2ea4d-935">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2ea4d-936">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2ea4d-937">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2ea4d-938">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2ea4d-939">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-940">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-941">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2ea4d-942">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="2ea4d-942">Dynamic grouping</span></span>
    * <span data-ttu-id="2ea4d-943">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-943">Pre-Post script</span></span>
    * <span data-ttu-id="2ea4d-944">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="2ea4d-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-945">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-946">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2ea4d-947">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2ea4d-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2ea4d-948">Az.KeyVault</span></span>
* <span data-ttu-id="2ea4d-949">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-950">Az.Network</span></span>
* <span data-ttu-id="2ea4d-951">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2ea4d-952">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-954">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2ea4d-955">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-956">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-957">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2ea4d-958">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-959">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-960">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-961">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-962">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2ea4d-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2ea4d-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2ea4d-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2ea4d-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2ea4d-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2ea4d-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2ea4d-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2ea4d-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-969">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-970">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="2ea4d-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="2ea4d-971">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-972">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-973">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2ea4d-974">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-975">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-976">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="2ea4d-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2ea4d-977">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2ea4d-978">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2ea4d-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2ea4d-979">Az.Cdn</span></span>
* <span data-ttu-id="2ea4d-980">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-981">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-982">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-983">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-984">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2ea4d-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2ea4d-985">Az.LogicApp</span></span>
* <span data-ttu-id="2ea4d-986">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-987">Az.Network</span></span>
* <span data-ttu-id="2ea4d-988">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-990">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2ea4d-991">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="2ea4d-991">SDK Update</span></span>
* <span data-ttu-id="2ea4d-992">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2ea4d-993">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-994">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-995">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2ea4d-996">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2ea4d-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2ea4d-997">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2ea4d-998">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2ea4d-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2ea4d-999">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2ea4d-1000">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1001">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1002">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2ea4d-1003">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1004">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-1005">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2ea4d-1006">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2ea4d-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="2ea4d-1008">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1009">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-1010">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2ea4d-1011">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2ea4d-1012">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2ea4d-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="2ea4d-1014">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1015">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1016">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2ea4d-1017">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2ea4d-1018">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2ea4d-1019">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-1021">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2ea4d-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1022">Az.EventHub</span></span>
* <span data-ttu-id="2ea4d-1023">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="2ea4d-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1024">Az.KeyVault</span></span>
* <span data-ttu-id="2ea4d-1025">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2ea4d-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1026">Az.LogicApp</span></span>
* <span data-ttu-id="2ea4d-1027">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2ea4d-1028">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2ea4d-1029">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2ea4d-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2ea4d-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2ea4d-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2ea4d-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2ea4d-1034">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2ea4d-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2ea4d-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2ea4d-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2ea4d-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2ea4d-1039">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2ea4d-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1040">Az.Monitor</span></span>
* <span data-ttu-id="2ea4d-1041">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1042">Az.Network</span></span>
* <span data-ttu-id="2ea4d-1043">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="2ea4d-1045">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2ea4d-1046">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="2ea4d-1047">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1048">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1049">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2ea4d-1050">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2ea4d-1051">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2ea4d-1052">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1053">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1054">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2ea4d-1055">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1056">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-1057">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2ea4d-1058">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1059">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-1060">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2ea4d-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="2ea4d-1062">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1063">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1064">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2ea4d-1065">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2ea4d-1066">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="2ea4d-1068">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1069">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1070">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="2ea4d-1071">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2ea4d-1072">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="2ea4d-1073">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1074">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1075">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2ea4d-1076">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2ea4d-1077">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2ea4d-1078">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1079">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-1080">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2ea4d-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="2ea4d-1082">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="2ea4d-1084">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2ea4d-1085">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1086">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-1087">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2ea4d-1088">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2ea4d-1089">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2ea4d-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1090">Az.Aks</span></span>
* <span data-ttu-id="2ea4d-1091">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2ea4d-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1092">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-1093">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2ea4d-1094">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2ea4d-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1095">Az.Cdn</span></span>
* <span data-ttu-id="2ea4d-1096">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1097">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1098">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2ea4d-1099">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2ea4d-1100">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2ea4d-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2ea4d-1102">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2ea4d-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1103">Az.DataFactory</span></span>
* <span data-ttu-id="2ea4d-1104">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-1106">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2ea4d-1107">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2ea4d-1108">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2ea4d-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1109">Az.IotHub</span></span>
* <span data-ttu-id="2ea4d-1110">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2ea4d-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1111">Az.KeyVault</span></span>
* <span data-ttu-id="2ea4d-1112">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1113">Az.Network</span></span>
* <span data-ttu-id="2ea4d-1114">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1115">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1116">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2ea4d-1117">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2ea4d-1118">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2ea4d-1119">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2ea4d-1120">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2ea4d-1121">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2ea4d-1122">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-1124">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2ea4d-1125">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1125">Fix some error messages.</span></span>
* <span data-ttu-id="2ea4d-1126">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2ea4d-1127">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2ea4d-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1128">Az.SignalR</span></span>
* <span data-ttu-id="2ea4d-1129">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1130">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1131">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2ea4d-1132">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2ea4d-1133">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2ea4d-1134">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1135">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-1136">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2ea4d-1137">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2ea4d-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2ea4d-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2ea4d-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="2ea4d-1141">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1142">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-1143">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2ea4d-1144">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2ea4d-1145">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2ea4d-1146">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2ea4d-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1147">Az.Accounts</span></span>
* <span data-ttu-id="2ea4d-1148">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1149">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1150">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2ea4d-1151">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2ea4d-1152">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-1154">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2ea4d-1155">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2ea4d-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1156">Az.EventGrid</span></span>
* <span data-ttu-id="2ea4d-1157">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2ea4d-1158">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2ea4d-1159">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2ea4d-1160">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2ea4d-1161">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2ea4d-1162">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2ea4d-1163">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2ea4d-1164">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2ea4d-1165">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2ea4d-1166">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="2ea4d-1167">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2ea4d-1168">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2ea4d-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1169">Az.IotHub</span></span>
* <span data-ttu-id="2ea4d-1170">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2ea4d-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1171">Az.LogicApp</span></span>
* <span data-ttu-id="2ea4d-1172">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1173">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1174">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2ea4d-1175">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2ea4d-1176">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2ea4d-1177">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2ea4d-1178">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2ea4d-1179">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2ea4d-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1180">Az.SignalR</span></span>
* <span data-ttu-id="2ea4d-1181">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1182">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1183">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2ea4d-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1184">Az.Storage</span></span>
* <span data-ttu-id="2ea4d-1185">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2ea4d-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="2ea4d-1187">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2ea4d-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1189">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-1190">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2ea4d-1191">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2ea4d-1192">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2ea4d-1193">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1193">General</span></span>

- <span data-ttu-id="2ea4d-1194">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="2ea4d-1195">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1195">Online help for each module</span></span>
- <span data-ttu-id="2ea4d-1196">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2ea4d-1197">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2ea4d-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1198">Az.Accounts</span></span>
- <span data-ttu-id="2ea4d-1199">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="2ea4d-1200">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2ea4d-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="2ea4d-1202">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1202">Fixes for #7002</span></span>
- <span data-ttu-id="2ea4d-1203">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2ea4d-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1204">Az.Batch</span></span>
- <span data-ttu-id="2ea4d-1205">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2ea4d-1206">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2ea4d-1207">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2ea4d-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1208">Az.Billing</span></span>
- <span data-ttu-id="2ea4d-1209">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2ea4d-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="2ea4d-1211">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2ea4d-1212">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2ea4d-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="2ea4d-1214">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2ea4d-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2ea4d-1216">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="2ea4d-1218">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2ea4d-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1219">Az.Monitor</span></span>
- <span data-ttu-id="2ea4d-1220">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2ea4d-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1221">Az.KeyVault</span></span>
- <span data-ttu-id="2ea4d-1222">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2ea4d-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="2ea4d-1224">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2ea4d-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1225">Az.Media</span></span>
- <span data-ttu-id="2ea4d-1226">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1227">Az.Network</span></span>
<span data-ttu-id="2ea4d-1228">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2ea4d-1229">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="2ea4d-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2ea4d-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2ea4d-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2ea4d-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2ea4d-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2ea4d-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2ea4d-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2ea4d-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2ea4d-1238">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2ea4d-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2ea4d-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2ea4d-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2ea4d-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2ea4d-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2ea4d-1244">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2ea4d-1245">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2ea4d-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2ea4d-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2ea4d-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2ea4d-1249">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2ea4d-1250">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2ea4d-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="2ea4d-1252">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2ea4d-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1253">Az.Profile</span></span>
- <span data-ttu-id="2ea4d-1254">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="2ea4d-1256">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2ea4d-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1257">Az.Resources</span></span>
- <span data-ttu-id="2ea4d-1258">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="2ea4d-1260">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2ea4d-1261">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2ea4d-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="2ea4d-1263">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2ea4d-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1264">Az.Sql</span></span>
- <span data-ttu-id="2ea4d-1265">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2ea4d-1266">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2ea4d-1267">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2ea4d-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1268">Az.Storage</span></span>
- <span data-ttu-id="2ea4d-1269">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2ea4d-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1270">Az.Websites</span></span>
- <span data-ttu-id="2ea4d-1271">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2ea4d-1272">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2ea4d-1273">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1273">General</span></span>

* <span data-ttu-id="2ea4d-1274">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2ea4d-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1275">Az.Compute</span></span>

* <span data-ttu-id="2ea4d-1276">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="2ea4d-1278">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2ea4d-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="2ea4d-1280">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="2ea4d-1281">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2ea4d-1282">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2ea4d-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="2ea4d-1284">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2ea4d-1285">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2ea4d-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1286">Az.Resources</span></span>

* <span data-ttu-id="2ea4d-1287">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2ea4d-1288">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2ea4d-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1289">Az.Sql</span></span>

* <span data-ttu-id="2ea4d-1290">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2ea4d-1291">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2ea4d-1292">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2ea4d-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1293">Az.Storage</span></span>

* <span data-ttu-id="2ea4d-1294">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2ea4d-1295">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2ea4d-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2ea4d-1297">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="2ea4d-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2ea4d-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2ea4d-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1300">Az.Websites</span></span>

* <span data-ttu-id="2ea4d-1301">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="2ea4d-1302">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2ea4d-1303">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2ea4d-1304">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2ea4d-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="2ea4d-1306">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2ea4d-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1307">Az.Automation</span></span>
* <span data-ttu-id="2ea4d-1308">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2ea4d-1309">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2ea4d-1310">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2ea4d-1311">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2ea4d-1312">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2ea4d-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1313">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1314">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2ea4d-1315">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2ea4d-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="2ea4d-1317">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2ea4d-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2ea4d-1319">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1320">Az.Network</span></span>
* <span data-ttu-id="2ea4d-1321">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2ea4d-1322">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2ea4d-1323">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="2ea4d-1324">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2ea4d-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2ea4d-1326">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2ea4d-1327">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2ea4d-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2ea4d-1329">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2ea4d-1330">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2ea4d-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1331">Az.Relay</span></span>
* <span data-ttu-id="2ea4d-1332">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2ea4d-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1333">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1334">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2ea4d-1335">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2ea4d-1336">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-1338">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2ea4d-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1339">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1340">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2ea4d-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2ea4d-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2ea4d-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2ea4d-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2ea4d-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2ea4d-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2ea4d-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2ea4d-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2ea4d-1349">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2ea4d-1350">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2ea4d-1351">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2ea4d-1352">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2ea4d-1353">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2ea4d-1354">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2ea4d-1355">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2ea4d-1356">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2ea4d-1357">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2ea4d-1358">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1358">General</span></span>
* <span data-ttu-id="2ea4d-1359">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2ea4d-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1360">Az.Profile</span></span>
* <span data-ttu-id="2ea4d-1361">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2ea4d-1362">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2ea4d-1363">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2ea4d-1364">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2ea4d-1365">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2ea4d-1366">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2ea4d-1367">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2ea4d-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="2ea4d-1369">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1370">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1371">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2ea4d-1372">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2ea4d-1373">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-1375">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2ea4d-1376">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2ea4d-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1377">Az.Insights</span></span>
* <span data-ttu-id="2ea4d-1378">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2ea4d-1379">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2ea4d-1380">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2ea4d-1381">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1382">Az.Network</span></span>
* <span data-ttu-id="2ea4d-1383">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2ea4d-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2ea4d-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2ea4d-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2ea4d-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2ea4d-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2ea4d-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2ea4d-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="2ea4d-1391">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1392">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1393">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2ea4d-1394">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2ea4d-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="2ea4d-1396">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2ea4d-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="2ea4d-1398">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2ea4d-1399">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2ea4d-1400">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2ea4d-1401">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2ea4d-1402">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2ea4d-1403">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2ea4d-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1404">Az.Profile</span></span>
* <span data-ttu-id="2ea4d-1405">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2ea4d-1406">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1407">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1408">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2ea4d-1409">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2ea4d-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="2ea4d-1411">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2ea4d-1412">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2ea4d-1413">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2ea4d-1414">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2ea4d-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1416">Az.Network</span></span>
* <span data-ttu-id="2ea4d-1417">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2ea4d-1418">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1419">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1420">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2ea4d-1421">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2ea4d-1422">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2ea4d-1423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1423">Azure.Storage</span></span>
* <span data-ttu-id="2ea4d-1424">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2ea4d-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2ea4d-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2ea4d-1427">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2ea4d-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="2ea4d-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="2ea4d-1430">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2ea4d-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1431">Az.Compute</span></span>
* <span data-ttu-id="2ea4d-1432">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2ea4d-1433">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2ea4d-1434">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2ea4d-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2ea4d-1436">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2ea4d-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1437">Az.Network</span></span>
* <span data-ttu-id="2ea4d-1438">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2ea4d-1439">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1439">new cmdlets added</span></span>
    - <span data-ttu-id="2ea4d-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2ea4d-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2ea4d-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2ea4d-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2ea4d-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2ea4d-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2ea4d-1446">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2ea4d-1447">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2ea4d-1448">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2ea4d-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1449">Az.RedisCache</span></span>
* <span data-ttu-id="2ea4d-1450">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2ea4d-1451">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2ea4d-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1452">Az.Resources</span></span>
* <span data-ttu-id="2ea4d-1453">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2ea4d-1454">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2ea4d-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1455">Az.Sql</span></span>
* <span data-ttu-id="2ea4d-1456">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2ea4d-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1457">Az.Websites</span></span>
* <span data-ttu-id="2ea4d-1458">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2ea4d-1459">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2ea4d-1460">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2ea4d-1461">Erste Version</span><span class="sxs-lookup"><span data-stu-id="2ea4d-1461">Initial Release</span></span>