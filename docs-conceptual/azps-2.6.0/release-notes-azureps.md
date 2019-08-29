---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052633"
---
## <a name="260---august-2019"></a><span data-ttu-id="bf77a-101">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="bf77a-102">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bf77a-102">General</span></span>
* <span data-ttu-id="bf77a-103">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf77a-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-104">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-105">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="bf77a-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="bf77a-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bf77a-106">Az.Aks</span></span>
* <span data-ttu-id="bf77a-107">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="bf77a-108">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="bf77a-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bf77a-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf77a-109">Az.ApiManagement</span></span>
* <span data-ttu-id="bf77a-110">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="bf77a-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="bf77a-111">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="bf77a-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="bf77a-112">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="bf77a-113">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="bf77a-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="bf77a-114">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bf77a-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bf77a-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf77a-115">Az.Batch</span></span>
* <span data-ttu-id="bf77a-116">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="bf77a-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf77a-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf77a-117">Az.Cdn</span></span>
* <span data-ttu-id="bf77a-118">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-119">Az.Compute</span></span>
* <span data-ttu-id="bf77a-120">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="bf77a-121">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="bf77a-122">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="bf77a-123">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="bf77a-124">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="bf77a-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="bf77a-125">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="bf77a-126">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="bf77a-127">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-128">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-129">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="bf77a-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="bf77a-130">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="bf77a-131">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bf77a-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="bf77a-132">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-134">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf77a-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-135">Az.EventHub</span></span>
* <span data-ttu-id="bf77a-136">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="bf77a-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="bf77a-137">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="bf77a-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="bf77a-138">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="bf77a-139">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="bf77a-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="bf77a-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bf77a-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bf77a-141">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf77a-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf77a-142">Az.Monitor</span></span>
* <span data-ttu-id="bf77a-143">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-144">Az.Network</span></span>
* <span data-ttu-id="bf77a-145">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="bf77a-146">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="bf77a-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="bf77a-147">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="bf77a-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="bf77a-148">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="bf77a-149">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="bf77a-150">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="bf77a-151">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="bf77a-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf77a-153">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="bf77a-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="bf77a-154">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-154">Added example</span></span>
    - <span data-ttu-id="bf77a-155">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="bf77a-156">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="bf77a-157">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-159">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-160">Az.Resources</span></span>
* <span data-ttu-id="bf77a-161">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="bf77a-162">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="bf77a-163">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bf77a-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="bf77a-164">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf77a-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf77a-165">Az.ServiceBus</span></span>
* <span data-ttu-id="bf77a-166">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="bf77a-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="bf77a-167">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="bf77a-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="bf77a-168">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="bf77a-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf77a-170">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="bf77a-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="bf77a-171">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="bf77a-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="bf77a-172">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="bf77a-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="bf77a-173">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="bf77a-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="bf77a-174">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="bf77a-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="bf77a-175">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="bf77a-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-176">Az.Sql</span></span>
* <span data-ttu-id="bf77a-177">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-178">Az.Storage</span></span>
* <span data-ttu-id="bf77a-179">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="bf77a-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="bf77a-180">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="bf77a-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="bf77a-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf77a-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="bf77a-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf77a-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="bf77a-183">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="bf77a-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="bf77a-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf77a-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-185">Az.Websites</span></span>
* <span data-ttu-id="bf77a-186">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="bf77a-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="bf77a-187">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-188">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-189">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="bf77a-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="bf77a-191">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="bf77a-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-192">Az.Automation</span></span>
* <span data-ttu-id="bf77a-193">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf77a-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf77a-195">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-196">Az.Compute</span></span>
* <span data-ttu-id="bf77a-197">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bf77a-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf77a-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bf77a-199">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="bf77a-200">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="bf77a-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-201">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-202">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="bf77a-203">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf77a-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-204">Az.EventHub</span></span>
* <span data-ttu-id="bf77a-205">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bf77a-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bf77a-206">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf77a-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf77a-207">Az.KeyVault</span></span>
* <span data-ttu-id="bf77a-208">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf77a-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf77a-209">Az.LogicApp</span></span>
* <span data-ttu-id="bf77a-210">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="bf77a-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="bf77a-211">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bf77a-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-212">Az.ManagedServices</span></span>
* <span data-ttu-id="bf77a-213">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-214">Az.Network</span></span>
* <span data-ttu-id="bf77a-215">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="bf77a-216">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-216">New cmdlets</span></span>
        - <span data-ttu-id="bf77a-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf77a-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf77a-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf77a-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bf77a-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf77a-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf77a-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf77a-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf77a-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf77a-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf77a-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf77a-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf77a-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="bf77a-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="bf77a-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf77a-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="bf77a-225">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf77a-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="bf77a-226">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="bf77a-227">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, um anzugeben, dass durch Aktivierung oder Deaktivierung Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden</span><span class="sxs-lookup"><span data-stu-id="bf77a-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="bf77a-228">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, um anzugeben, dass durch Aktivierung oder Deaktivierung Netzwerkrichtlinien auf den privaten Verknüpfungsdienst in diesem Subnetz angewendet werden</span><span class="sxs-lookup"><span data-stu-id="bf77a-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="bf77a-229">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="bf77a-230">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="bf77a-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="bf77a-231">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-231">Updated cmdlets</span></span>
        - <span data-ttu-id="bf77a-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bf77a-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bf77a-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bf77a-235">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bf77a-236">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="bf77a-237">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bf77a-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="bf77a-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bf77a-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bf77a-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="bf77a-241">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="bf77a-242">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf77a-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="bf77a-243">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="bf77a-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf77a-245">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="bf77a-246">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-248">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bf77a-249">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="bf77a-250">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="bf77a-251">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bf77a-252">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="bf77a-253">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bf77a-254">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="bf77a-255">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bf77a-256">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="bf77a-257">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-258">Az.Resources</span></span>
- <span data-ttu-id="bf77a-259">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="bf77a-260">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf77a-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf77a-261">Az.ServiceBus</span></span>
* <span data-ttu-id="bf77a-262">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bf77a-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bf77a-263">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-264">Az.Sql</span></span>
* <span data-ttu-id="bf77a-265">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="bf77a-266">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="bf77a-267">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-268">Az.Storage</span></span>
* <span data-ttu-id="bf77a-269">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bf77a-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bf77a-270">Az.StorageSync</span></span>
* <span data-ttu-id="bf77a-271">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="bf77a-272">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-273">Az.Websites</span></span>
* <span data-ttu-id="bf77a-274">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="bf77a-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="bf77a-275">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="bf77a-276">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="bf77a-277">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-278">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-279">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="bf77a-280">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="bf77a-281">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="bf77a-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bf77a-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bf77a-282">Az.Advisor</span></span>
* <span data-ttu-id="bf77a-283">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bf77a-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="bf77a-284">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="bf77a-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bf77a-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf77a-285">Az.ApiManagement</span></span>
* <span data-ttu-id="bf77a-286">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="bf77a-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="bf77a-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="bf77a-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="bf77a-288">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="bf77a-289">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="bf77a-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="bf77a-290">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="bf77a-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="bf77a-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="bf77a-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="bf77a-292">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-293">Az.Automation</span></span>
* <span data-ttu-id="bf77a-294">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-295">Az.Compute</span></span>
* <span data-ttu-id="bf77a-296">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-297">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-298">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bf77a-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf77a-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf77a-299">Az.EventGrid</span></span>
* <span data-ttu-id="bf77a-300">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf77a-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-301">Az.IotHub</span></span>
* <span data-ttu-id="bf77a-302">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-303">Az.Network</span></span>
* <span data-ttu-id="bf77a-304">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="bf77a-305">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bf77a-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf77a-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf77a-307">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="bf77a-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="bf77a-308">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="bf77a-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf77a-310">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-312">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="bf77a-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-313">Az.Resources</span></span>
    - <span data-ttu-id="bf77a-314">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="bf77a-315">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="bf77a-316">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="bf77a-317">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf77a-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf77a-318">Az.ServiceBus</span></span>
* <span data-ttu-id="bf77a-319">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="bf77a-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-320">Az.Sql</span></span>
* <span data-ttu-id="bf77a-321">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="bf77a-322">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="bf77a-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bf77a-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bf77a-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bf77a-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bf77a-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bf77a-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bf77a-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bf77a-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bf77a-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bf77a-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bf77a-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bf77a-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="bf77a-329">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-330">Az.Storage</span></span>
* <span data-ttu-id="bf77a-331">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="bf77a-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="bf77a-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bf77a-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="bf77a-333">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="bf77a-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="bf77a-334">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="bf77a-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="bf77a-335">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="bf77a-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="bf77a-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bf77a-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bf77a-338">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="bf77a-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="bf77a-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bf77a-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="bf77a-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bf77a-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bf77a-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bf77a-341">Az.StorageSync</span></span>
* <span data-ttu-id="bf77a-342">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="bf77a-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="bf77a-343">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-344">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-345">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="bf77a-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="bf77a-346">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="bf77a-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="bf77a-347">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="bf77a-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf77a-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="bf77a-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="bf77a-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-350">Az.Compute</span></span>
* <span data-ttu-id="bf77a-351">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="bf77a-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="bf77a-352">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="bf77a-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bf77a-353">Az.Dns</span></span>
* <span data-ttu-id="bf77a-354">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf77a-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf77a-355">Az.EventGrid</span></span>
* <span data-ttu-id="bf77a-356">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="bf77a-357">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bf77a-357">New cmdlets:</span></span>
    - <span data-ttu-id="bf77a-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bf77a-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bf77a-359">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="bf77a-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bf77a-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bf77a-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bf77a-361">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bf77a-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="bf77a-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bf77a-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bf77a-363">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="bf77a-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bf77a-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bf77a-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bf77a-365">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="bf77a-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bf77a-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bf77a-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bf77a-367">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="bf77a-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bf77a-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bf77a-369">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="bf77a-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="bf77a-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bf77a-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="bf77a-371">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bf77a-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="bf77a-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bf77a-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bf77a-373">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="bf77a-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="bf77a-374">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bf77a-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="bf77a-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bf77a-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="bf77a-376">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bf77a-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bf77a-377">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bf77a-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bf77a-378">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="bf77a-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="bf77a-379">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bf77a-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="bf77a-380">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="bf77a-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="bf77a-381">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="bf77a-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="bf77a-382">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="bf77a-383">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="bf77a-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="bf77a-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bf77a-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="bf77a-385">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="bf77a-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="bf77a-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="bf77a-387">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bf77a-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="bf77a-388">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bf77a-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf77a-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf77a-389">Az.FrontDoor</span></span>
* <span data-ttu-id="bf77a-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="bf77a-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="bf77a-391">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="bf77a-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bf77a-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="bf77a-393">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-394">Az.Network</span></span>
* <span data-ttu-id="bf77a-395">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="bf77a-396">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-396">New cmdlets</span></span>
        - <span data-ttu-id="bf77a-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="bf77a-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="bf77a-398">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="bf77a-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="bf77a-399">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-399">New cmdlets</span></span> 
        - <span data-ttu-id="bf77a-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="bf77a-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="bf77a-401">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="bf77a-402">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-402">New cmdlets</span></span> 
        - <span data-ttu-id="bf77a-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf77a-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="bf77a-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf77a-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bf77a-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf77a-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bf77a-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="bf77a-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf77a-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bf77a-408">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="bf77a-409">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-409">New cmdlets</span></span>
        - <span data-ttu-id="bf77a-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf77a-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf77a-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf77a-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf77a-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf77a-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf77a-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="bf77a-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="bf77a-414">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="bf77a-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="bf77a-415">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bf77a-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="bf77a-416">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bf77a-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="bf77a-417">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="bf77a-418">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="bf77a-419">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="bf77a-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="bf77a-420">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="bf77a-421">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="bf77a-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="bf77a-422">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="bf77a-423">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="bf77a-424">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="bf77a-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="bf77a-425">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="bf77a-426">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="bf77a-427">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="bf77a-428">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="bf77a-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="bf77a-429">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="bf77a-430">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="bf77a-431">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="bf77a-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="bf77a-432">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="bf77a-433">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="bf77a-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="bf77a-434">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bf77a-435">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bf77a-436">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf77a-438">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="bf77a-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-439">Az.Resources</span></span>
* <span data-ttu-id="bf77a-440">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="bf77a-441">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bf77a-442">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bf77a-443">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bf77a-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf77a-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf77a-445">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="bf77a-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-446">Az.Sql</span></span>
* <span data-ttu-id="bf77a-447">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="bf77a-448">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="bf77a-449">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="bf77a-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf77a-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bf77a-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf77a-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bf77a-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf77a-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bf77a-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bf77a-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="bf77a-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bf77a-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-455">Az.Storage</span></span>
* <span data-ttu-id="bf77a-456">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bf77a-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="bf77a-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="bf77a-458">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="bf77a-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="bf77a-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bf77a-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-460">Az.Websites</span></span>
* <span data-ttu-id="bf77a-461">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="bf77a-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="bf77a-462">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="bf77a-463">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="bf77a-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf77a-464">Az.Cdn</span></span>
* <span data-ttu-id="bf77a-465">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-466">Az.Compute</span></span>
* <span data-ttu-id="bf77a-467">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bf77a-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="bf77a-468">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf77a-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf77a-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-469">Az.EventHub</span></span>
* <span data-ttu-id="bf77a-470">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="bf77a-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="bf77a-471">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="bf77a-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-472">Az.Network</span></span>
* <span data-ttu-id="bf77a-473">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="bf77a-474">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf77a-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf77a-476">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="bf77a-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-478">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf77a-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf77a-479">Az.ServiceBus</span></span>
* <span data-ttu-id="bf77a-480">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="bf77a-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf77a-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf77a-482">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="bf77a-483">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-484">Az.Sql</span></span>
* <span data-ttu-id="bf77a-485">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bf77a-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="bf77a-486">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bf77a-487">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="bf77a-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="bf77a-488">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="bf77a-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-489">Az.Websites</span></span>
* <span data-ttu-id="bf77a-490">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="bf77a-491">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bf77a-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf77a-492">Az.ApiManagement</span></span>
* <span data-ttu-id="bf77a-493">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="bf77a-494">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="bf77a-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="bf77a-495">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bf77a-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="bf77a-496">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="bf77a-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="bf77a-497">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="bf77a-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="bf77a-498">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="bf77a-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="bf77a-499">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bf77a-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="bf77a-500">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bf77a-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="bf77a-501">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="bf77a-502">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="bf77a-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="bf77a-503">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="bf77a-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="bf77a-504">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="bf77a-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="bf77a-505">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="bf77a-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="bf77a-506">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="bf77a-507">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="bf77a-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="bf77a-508">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="bf77a-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="bf77a-509">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="bf77a-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="bf77a-510">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="bf77a-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="bf77a-511">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="bf77a-512">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="bf77a-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="bf77a-513">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="bf77a-514">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="bf77a-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="bf77a-515">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="bf77a-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="bf77a-516">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="bf77a-517">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="bf77a-518">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="bf77a-519">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="bf77a-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="bf77a-520">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="bf77a-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="bf77a-521">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="bf77a-522">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="bf77a-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="bf77a-523">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="bf77a-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="bf77a-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="bf77a-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="bf77a-525">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="bf77a-526">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bf77a-527">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="bf77a-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="bf77a-528">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="bf77a-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="bf77a-529">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="bf77a-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="bf77a-530">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="bf77a-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="bf77a-531">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="bf77a-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="bf77a-532">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="bf77a-533">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="bf77a-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bf77a-534">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="bf77a-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="bf77a-535">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="bf77a-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="bf77a-536">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bf77a-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="bf77a-537">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bf77a-538">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="bf77a-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bf77a-539">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="bf77a-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="bf77a-540">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bf77a-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="bf77a-541">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="bf77a-542">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="bf77a-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="bf77a-543">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="bf77a-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="bf77a-544">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="bf77a-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="bf77a-545">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="bf77a-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="bf77a-546">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="bf77a-547">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="bf77a-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="bf77a-548">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="bf77a-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="bf77a-549">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bf77a-550">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bf77a-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bf77a-551">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bf77a-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bf77a-552">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bf77a-553">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bf77a-554">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bf77a-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bf77a-555">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bf77a-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bf77a-556">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bf77a-557">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="bf77a-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="bf77a-558">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="bf77a-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="bf77a-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="bf77a-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="bf77a-560">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="bf77a-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="bf77a-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="bf77a-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="bf77a-562">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="bf77a-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="bf77a-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="bf77a-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="bf77a-564">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="bf77a-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="bf77a-565">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="bf77a-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="bf77a-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="bf77a-567">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="bf77a-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="bf77a-568">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="bf77a-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="bf77a-569">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="bf77a-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-570">Az.Automation</span></span>
* <span data-ttu-id="bf77a-571">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf77a-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="bf77a-572">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="bf77a-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="bf77a-573">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="bf77a-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="bf77a-574">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="bf77a-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="bf77a-575">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="bf77a-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="bf77a-576">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="bf77a-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="bf77a-577">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="bf77a-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-578">Az.Compute</span></span>
* <span data-ttu-id="bf77a-579">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="bf77a-580">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-582">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="bf77a-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf77a-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf77a-583">Az.Monitor</span></span>
* <span data-ttu-id="bf77a-584">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="bf77a-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-585">Az.Network</span></span>
* <span data-ttu-id="bf77a-586">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="bf77a-587">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bf77a-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="bf77a-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf77a-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="bf77a-589">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bf77a-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-590">Az.Resources</span></span>
* <span data-ttu-id="bf77a-591">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-592">Az.Sql</span></span>
* <span data-ttu-id="bf77a-593">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="bf77a-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="bf77a-594">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-595">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-596">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="bf77a-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf77a-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf77a-598">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="bf77a-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="bf77a-599">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="bf77a-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-600">Az.Compute</span></span>
* <span data-ttu-id="bf77a-601">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="bf77a-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="bf77a-602">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bf77a-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="bf77a-603">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="bf77a-604">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="bf77a-605">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="bf77a-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="bf77a-606">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="bf77a-607">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="bf77a-607">Breaking changes</span></span>
    - <span data-ttu-id="bf77a-608">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="bf77a-609">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="bf77a-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="bf77a-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="bf77a-611">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="bf77a-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bf77a-612">Az.Dns</span></span>
* <span data-ttu-id="bf77a-613">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="bf77a-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="bf77a-614">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="bf77a-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="bf77a-615">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf77a-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf77a-616">Az.FrontDoor</span></span>
* <span data-ttu-id="bf77a-617">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="bf77a-618">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="bf77a-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="bf77a-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf77a-619">Az.HDInsight</span></span>
* <span data-ttu-id="bf77a-620">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="bf77a-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="bf77a-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf77a-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="bf77a-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf77a-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bf77a-623">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="bf77a-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bf77a-624">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="bf77a-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="bf77a-625">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bf77a-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="bf77a-626">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf77a-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf77a-627">Az.Monitor</span></span>
* <span data-ttu-id="bf77a-628">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="bf77a-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="bf77a-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bf77a-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="bf77a-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="bf77a-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="bf77a-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="bf77a-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="bf77a-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="bf77a-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="bf77a-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bf77a-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="bf77a-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="bf77a-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="bf77a-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf77a-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf77a-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf77a-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf77a-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf77a-640">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="bf77a-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="bf77a-641">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="bf77a-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-642">Az.Network</span></span>
* <span data-ttu-id="bf77a-643">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="bf77a-644">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-644">New cmdlets</span></span>
        - <span data-ttu-id="bf77a-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf77a-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="bf77a-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf77a-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="bf77a-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf77a-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="bf77a-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf77a-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="bf77a-649">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-649">Updated cmdlets</span></span>
        - <span data-ttu-id="bf77a-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bf77a-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="bf77a-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bf77a-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="bf77a-652">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="bf77a-653">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="bf77a-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="bf77a-654">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="bf77a-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf77a-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf77a-656">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="bf77a-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="bf77a-657">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="bf77a-658">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="bf77a-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-660">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="bf77a-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="bf77a-661">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="bf77a-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="bf77a-662">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="bf77a-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="bf77a-663">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="bf77a-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="bf77a-664">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="bf77a-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="bf77a-665">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="bf77a-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="bf77a-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bf77a-666">Az.Relay</span></span>
* <span data-ttu-id="bf77a-667">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="bf77a-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf77a-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf77a-668">Az.ServiceBus</span></span>
* <span data-ttu-id="bf77a-669">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-670">Az.Storage</span></span>
* <span data-ttu-id="bf77a-671">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="bf77a-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="bf77a-672">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bf77a-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="bf77a-673">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="bf77a-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="bf77a-675">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="bf77a-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="bf77a-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="bf77a-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="bf77a-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-679">Az.Websites</span></span>
* <span data-ttu-id="bf77a-680">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="bf77a-681">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="bf77a-682">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf77a-683">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="bf77a-683">Highlights since the last major release</span></span>
* <span data-ttu-id="bf77a-684">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="bf77a-684">General availability of `Az` module</span></span>
* <span data-ttu-id="bf77a-685">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="bf77a-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bf77a-686">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="bf77a-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bf77a-687">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bf77a-688">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf77a-689">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bf77a-690">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf77a-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-691">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-692">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="bf77a-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bf77a-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf77a-693">Az.Batch</span></span>
* <span data-ttu-id="bf77a-694">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf77a-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf77a-695">Az.Cdn</span></span>
* <span data-ttu-id="bf77a-696">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf77a-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf77a-698">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-699">Az.Compute</span></span>
* <span data-ttu-id="bf77a-700">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="bf77a-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="bf77a-701">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf77a-702">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-703">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-704">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="bf77a-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-706">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf77a-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf77a-707">Az.EventGrid</span></span>
* <span data-ttu-id="bf77a-708">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bf77a-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf77a-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-709">Az.EventHub</span></span>
* <span data-ttu-id="bf77a-710">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="bf77a-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf77a-711">Az.HDInsight</span></span>
* <span data-ttu-id="bf77a-712">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf77a-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-713">Az.IotHub</span></span>
* <span data-ttu-id="bf77a-714">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf77a-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf77a-715">Az.KeyVault</span></span>
* <span data-ttu-id="bf77a-716">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf77a-717">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="bf77a-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bf77a-718">Az.MachineLearning</span></span>
* <span data-ttu-id="bf77a-719">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="bf77a-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bf77a-720">Az.Media</span></span>
* <span data-ttu-id="bf77a-721">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf77a-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf77a-722">Az.Monitor</span></span>
  * <span data-ttu-id="bf77a-723">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="bf77a-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="bf77a-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="bf77a-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="bf77a-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="bf77a-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="bf77a-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bf77a-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bf77a-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bf77a-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bf77a-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bf77a-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="bf77a-729">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-730">Az.Network</span></span>
* <span data-ttu-id="bf77a-731">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf77a-732">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="bf77a-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="bf77a-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="bf77a-734">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf77a-736">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="bf77a-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bf77a-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="bf77a-738">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-740">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf77a-741">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="bf77a-742">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="bf77a-743">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bf77a-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bf77a-744">Az.RedisCache</span></span>
* <span data-ttu-id="bf77a-745">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-746">Az.Resources</span></span>
* <span data-ttu-id="bf77a-747">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-748">Az.Sql</span></span>
* <span data-ttu-id="bf77a-749">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="bf77a-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="bf77a-750">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf77a-751">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="bf77a-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="bf77a-752">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="bf77a-753">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="bf77a-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="bf77a-754">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="bf77a-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="bf77a-755">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-756">Az.Websites</span></span>
* <span data-ttu-id="bf77a-757">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="bf77a-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="bf77a-758">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf77a-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf77a-759">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="bf77a-760">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="bf77a-761">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf77a-762">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="bf77a-762">Highlights since the last major release</span></span>
* <span data-ttu-id="bf77a-763">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="bf77a-763">General availability of `Az` module</span></span>
* <span data-ttu-id="bf77a-764">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="bf77a-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bf77a-765">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="bf77a-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bf77a-766">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bf77a-767">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf77a-768">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bf77a-769">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf77a-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-770">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-771">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="bf77a-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bf77a-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="bf77a-773">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="bf77a-774">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-775">Az.Automation</span></span>
* <span data-ttu-id="bf77a-776">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="bf77a-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="bf77a-777">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bf77a-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="bf77a-778">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="bf77a-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-779">Az.Compute</span></span>
* <span data-ttu-id="bf77a-780">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bf77a-781">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="bf77a-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="bf77a-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="bf77a-783">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="bf77a-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-784">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-785">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="bf77a-786">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-787">Az.Resources</span></span>
* <span data-ttu-id="bf77a-788">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bf77a-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="bf77a-789">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bf77a-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="bf77a-790">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="bf77a-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="bf77a-791">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bf77a-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="bf77a-792">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="bf77a-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="bf77a-793">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bf77a-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-794">Az.Sql</span></span>
* <span data-ttu-id="bf77a-795">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="bf77a-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-796">Az.Storage</span></span>
* <span data-ttu-id="bf77a-797">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="bf77a-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="bf77a-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf77a-798">New-AzStorageContext</span></span>
* <span data-ttu-id="bf77a-799">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="bf77a-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="bf77a-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bf77a-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bf77a-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bf77a-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bf77a-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf77a-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="bf77a-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf77a-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="bf77a-804">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="bf77a-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="bf77a-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf77a-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bf77a-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf77a-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bf77a-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bf77a-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="bf77a-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bf77a-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="bf77a-809">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf77a-810">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="bf77a-810">Highlights since the last major release</span></span>
* <span data-ttu-id="bf77a-811">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="bf77a-811">General availability of `Az` module</span></span>
* <span data-ttu-id="bf77a-812">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="bf77a-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bf77a-813">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="bf77a-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bf77a-814">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bf77a-815">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf77a-816">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bf77a-817">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-818">Az.Automation</span></span>
* <span data-ttu-id="bf77a-819">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="bf77a-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="bf77a-820">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="bf77a-820">Dynamic grouping</span></span>
    * <span data-ttu-id="bf77a-821">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="bf77a-821">Pre-Post script</span></span>
    * <span data-ttu-id="bf77a-822">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="bf77a-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-823">Az.Compute</span></span>
* <span data-ttu-id="bf77a-824">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="bf77a-825">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf77a-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf77a-826">Az.KeyVault</span></span>
* <span data-ttu-id="bf77a-827">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-828">Az.Network</span></span>
* <span data-ttu-id="bf77a-829">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="bf77a-830">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-832">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bf77a-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="bf77a-833">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-834">Az.Resources</span></span>
* <span data-ttu-id="bf77a-835">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="bf77a-836">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bf77a-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-837">Az.Sql</span></span>
* <span data-ttu-id="bf77a-838">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-839">Az.Storage</span></span>
* <span data-ttu-id="bf77a-840">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="bf77a-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bf77a-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bf77a-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bf77a-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bf77a-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bf77a-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bf77a-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="bf77a-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="bf77a-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="bf77a-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="bf77a-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-847">Az.Websites</span></span>
* <span data-ttu-id="bf77a-848">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="bf77a-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="bf77a-849">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-850">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-851">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="bf77a-852">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-853">Az.Automation</span></span>
* <span data-ttu-id="bf77a-854">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="bf77a-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="bf77a-855">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="bf77a-856">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf77a-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf77a-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf77a-857">Az.Cdn</span></span>
* <span data-ttu-id="bf77a-858">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="bf77a-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-859">Az.Compute</span></span>
* <span data-ttu-id="bf77a-860">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-861">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-862">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf77a-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf77a-863">Az.LogicApp</span></span>
* <span data-ttu-id="bf77a-864">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="bf77a-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-865">Az.Network</span></span>
* <span data-ttu-id="bf77a-866">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-868">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="bf77a-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="bf77a-869">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="bf77a-869">SDK Update</span></span>
* <span data-ttu-id="bf77a-870">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="bf77a-871">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-872">Az.Resources</span></span>
* <span data-ttu-id="bf77a-873">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="bf77a-874">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="bf77a-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="bf77a-875">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="bf77a-876">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="bf77a-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="bf77a-877">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="bf77a-878">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="bf77a-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-879">Az.Sql</span></span>
* <span data-ttu-id="bf77a-880">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="bf77a-881">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-882">Az.Storage</span></span>
* <span data-ttu-id="bf77a-883">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf77a-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="bf77a-884">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="bf77a-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="bf77a-886">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-887">Az.Automation</span></span>
* <span data-ttu-id="bf77a-888">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="bf77a-889">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="bf77a-890">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bf77a-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf77a-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf77a-892">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf77a-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-893">Az.Compute</span></span>
* <span data-ttu-id="bf77a-894">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="bf77a-895">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="bf77a-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="bf77a-896">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="bf77a-897">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="bf77a-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-899">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf77a-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-900">Az.EventHub</span></span>
* <span data-ttu-id="bf77a-901">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="bf77a-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf77a-902">Az.KeyVault</span></span>
* <span data-ttu-id="bf77a-903">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf77a-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf77a-904">Az.LogicApp</span></span>
* <span data-ttu-id="bf77a-905">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="bf77a-906">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="bf77a-907">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="bf77a-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="bf77a-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf77a-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bf77a-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf77a-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bf77a-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf77a-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bf77a-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf77a-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="bf77a-912">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="bf77a-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bf77a-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bf77a-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bf77a-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="bf77a-917">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf77a-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf77a-918">Az.Monitor</span></span>
* <span data-ttu-id="bf77a-919">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-920">Az.Network</span></span>
* <span data-ttu-id="bf77a-921">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf77a-923">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="bf77a-924">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="bf77a-925">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="bf77a-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="bf77a-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-926">Az.Resources</span></span>
* <span data-ttu-id="bf77a-927">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bf77a-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bf77a-928">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bf77a-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="bf77a-929">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="bf77a-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="bf77a-930">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="bf77a-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-931">Az.Sql</span></span>
* <span data-ttu-id="bf77a-932">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="bf77a-933">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="bf77a-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-934">Az.Websites</span></span>
* <span data-ttu-id="bf77a-935">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="bf77a-936">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-937">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-938">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="bf77a-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bf77a-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-939">Az.AnalysisServices</span></span>
<span data-ttu-id="bf77a-940">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="bf77a-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-941">Az.Compute</span></span>
* <span data-ttu-id="bf77a-942">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="bf77a-943">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="bf77a-944">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-945">Az.RecoveryServices</span></span>
<span data-ttu-id="bf77a-946">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="bf77a-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-947">Az.Resources</span></span>
* <span data-ttu-id="bf77a-948">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="bf77a-949">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bf77a-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bf77a-950">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="bf77a-951">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bf77a-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-952">Az.Sql</span></span>
* <span data-ttu-id="bf77a-953">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="bf77a-954">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="bf77a-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="bf77a-955">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="bf77a-956">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-957">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-958">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="bf77a-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bf77a-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="bf77a-960">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="bf77a-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf77a-962">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="bf77a-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="bf77a-963">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-964">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-965">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf77a-966">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf77a-967">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="bf77a-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bf77a-968">Az.Aks</span></span>
* <span data-ttu-id="bf77a-969">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf77a-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-970">Az.Automation</span></span>
* <span data-ttu-id="bf77a-971">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="bf77a-972">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf77a-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf77a-973">Az.Cdn</span></span>
* <span data-ttu-id="bf77a-974">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-975">Az.Compute</span></span>
* <span data-ttu-id="bf77a-976">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="bf77a-977">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="bf77a-978">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bf77a-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf77a-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bf77a-980">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf77a-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf77a-981">Az.DataFactory</span></span>
* <span data-ttu-id="bf77a-982">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-984">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="bf77a-985">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="bf77a-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="bf77a-986">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf77a-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-987">Az.IotHub</span></span>
* <span data-ttu-id="bf77a-988">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf77a-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf77a-989">Az.KeyVault</span></span>
* <span data-ttu-id="bf77a-990">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-991">Az.Network</span></span>
* <span data-ttu-id="bf77a-992">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-993">Az.Resources</span></span>
* <span data-ttu-id="bf77a-994">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="bf77a-995">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="bf77a-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="bf77a-996">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="bf77a-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="bf77a-997">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="bf77a-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="bf77a-998">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="bf77a-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="bf77a-999">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="bf77a-1000">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="bf77a-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf77a-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf77a-1002">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="bf77a-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="bf77a-1003">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1003">Fix some error messages.</span></span>
* <span data-ttu-id="bf77a-1004">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="bf77a-1005">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bf77a-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bf77a-1006">Az.SignalR</span></span>
* <span data-ttu-id="bf77a-1007">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-1008">Az.Sql</span></span>
* <span data-ttu-id="bf77a-1009">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf77a-1010">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="bf77a-1011">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="bf77a-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="bf77a-1012">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="bf77a-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-1013">Az.Storage</span></span>
* <span data-ttu-id="bf77a-1014">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf77a-1015">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="bf77a-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bf77a-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="bf77a-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bf77a-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="bf77a-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bf77a-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="bf77a-1019">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-1020">Az.Websites</span></span>
* <span data-ttu-id="bf77a-1021">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf77a-1022">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="bf77a-1023">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="bf77a-1024">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="bf77a-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf77a-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-1025">Az.Accounts</span></span>
* <span data-ttu-id="bf77a-1026">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-1027">Az.Compute</span></span>
* <span data-ttu-id="bf77a-1028">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="bf77a-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="bf77a-1029">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="bf77a-1030">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-1032">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="bf77a-1033">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf77a-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf77a-1034">Az.EventGrid</span></span>
* <span data-ttu-id="bf77a-1035">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="bf77a-1036">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="bf77a-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="bf77a-1037">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bf77a-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bf77a-1038">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="bf77a-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bf77a-1039">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="bf77a-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bf77a-1040">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="bf77a-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="bf77a-1041">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bf77a-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bf77a-1042">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="bf77a-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bf77a-1043">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="bf77a-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bf77a-1044">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="bf77a-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="bf77a-1045">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="bf77a-1046">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="bf77a-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf77a-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf77a-1047">Az.IotHub</span></span>
* <span data-ttu-id="bf77a-1048">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf77a-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf77a-1049">Az.LogicApp</span></span>
* <span data-ttu-id="bf77a-1050">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="bf77a-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1051">Az.Resources</span></span>
* <span data-ttu-id="bf77a-1052">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="bf77a-1053">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="bf77a-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="bf77a-1054">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bf77a-1055">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="bf77a-1056">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="bf77a-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="bf77a-1057">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="bf77a-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bf77a-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bf77a-1058">Az.SignalR</span></span>
* <span data-ttu-id="bf77a-1059">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-1060">Az.Sql</span></span>
* <span data-ttu-id="bf77a-1061">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf77a-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-1062">Az.Storage</span></span>
* <span data-ttu-id="bf77a-1063">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="bf77a-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf77a-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="bf77a-1065">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="bf77a-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="bf77a-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bf77a-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-1067">Az.Websites</span></span>
* <span data-ttu-id="bf77a-1068">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="bf77a-1069">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="bf77a-1070">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="bf77a-1071">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bf77a-1071">General</span></span>

- <span data-ttu-id="bf77a-1072">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="bf77a-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="bf77a-1073">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="bf77a-1073">Online help for each module</span></span>
- <span data-ttu-id="bf77a-1074">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="bf77a-1075">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="bf77a-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf77a-1076">Az.Accounts</span></span>
- <span data-ttu-id="bf77a-1077">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="bf77a-1078">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="bf77a-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bf77a-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf77a-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="bf77a-1080">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="bf77a-1080">Fixes for #7002</span></span>
- <span data-ttu-id="bf77a-1081">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="bf77a-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf77a-1082">Az.Batch</span></span>
- <span data-ttu-id="bf77a-1083">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="bf77a-1084">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="bf77a-1085">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="bf77a-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bf77a-1086">Az.Billing</span></span>
- <span data-ttu-id="bf77a-1087">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="bf77a-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="bf77a-1089">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="bf77a-1090">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bf77a-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="bf77a-1092">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="bf77a-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="bf77a-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="bf77a-1094">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="bf77a-1096">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="bf77a-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf77a-1097">Az.Monitor</span></span>
- <span data-ttu-id="bf77a-1098">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="bf77a-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf77a-1099">Az.KeyVault</span></span>
- <span data-ttu-id="bf77a-1100">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="bf77a-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bf77a-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="bf77a-1102">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="bf77a-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="bf77a-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bf77a-1103">Az.Media</span></span>
- <span data-ttu-id="bf77a-1104">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bf77a-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-1105">Az.Network</span></span>
<span data-ttu-id="bf77a-1106">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="bf77a-1107">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bf77a-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="bf77a-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf77a-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf77a-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf77a-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf77a-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf77a-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf77a-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf77a-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf77a-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf77a-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf77a-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="bf77a-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bf77a-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="bf77a-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf77a-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="bf77a-1116">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="bf77a-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf77a-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="bf77a-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bf77a-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf77a-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bf77a-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="bf77a-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="bf77a-1122">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="bf77a-1123">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf77a-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="bf77a-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf77a-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bf77a-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf77a-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bf77a-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf77a-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="bf77a-1127">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="bf77a-1128">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="bf77a-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="bf77a-1130">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="bf77a-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1131">Az.Profile</span></span>
- <span data-ttu-id="bf77a-1132">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="bf77a-1134">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="bf77a-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1135">Az.Resources</span></span>
- <span data-ttu-id="bf77a-1136">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bf77a-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="bf77a-1138">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="bf77a-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="bf77a-1139">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="bf77a-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="bf77a-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="bf77a-1141">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="bf77a-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="bf77a-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-1142">Az.Sql</span></span>
- <span data-ttu-id="bf77a-1143">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="bf77a-1144">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="bf77a-1145">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="bf77a-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-1146">Az.Storage</span></span>
- <span data-ttu-id="bf77a-1147">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bf77a-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-1148">Az.Websites</span></span>
- <span data-ttu-id="bf77a-1149">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf77a-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="bf77a-1150">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="bf77a-1151">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bf77a-1151">General</span></span>

* <span data-ttu-id="bf77a-1152">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="bf77a-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="bf77a-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-1153">Az.Compute</span></span>

* <span data-ttu-id="bf77a-1154">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="bf77a-1156">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="bf77a-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf77a-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="bf77a-1158">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="bf77a-1159">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="bf77a-1160">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bf77a-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="bf77a-1162">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="bf77a-1163">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="bf77a-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1164">Az.Resources</span></span>

* <span data-ttu-id="bf77a-1165">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="bf77a-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="bf77a-1166">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="bf77a-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-1167">Az.Sql</span></span>

* <span data-ttu-id="bf77a-1168">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="bf77a-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="bf77a-1169">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="bf77a-1170">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="bf77a-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-1171">Az.Storage</span></span>

* <span data-ttu-id="bf77a-1172">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="bf77a-1173">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="bf77a-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bf77a-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bf77a-1175">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="bf77a-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bf77a-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="bf77a-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bf77a-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bf77a-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-1178">Az.Websites</span></span>

* <span data-ttu-id="bf77a-1179">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf77a-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="bf77a-1180">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="bf77a-1181">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="bf77a-1182">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bf77a-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf77a-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="bf77a-1184">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="bf77a-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf77a-1185">Az.Automation</span></span>
* <span data-ttu-id="bf77a-1186">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf77a-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="bf77a-1187">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="bf77a-1188">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="bf77a-1189">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="bf77a-1190">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="bf77a-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-1191">Az.Compute</span></span>
* <span data-ttu-id="bf77a-1192">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="bf77a-1193">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bf77a-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="bf77a-1195">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="bf77a-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bf77a-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bf77a-1197">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bf77a-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-1198">Az.Network</span></span>
* <span data-ttu-id="bf77a-1199">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bf77a-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="bf77a-1200">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="bf77a-1201">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="bf77a-1202">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="bf77a-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bf77a-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bf77a-1204">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="bf77a-1205">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="bf77a-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bf77a-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bf77a-1207">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="bf77a-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="bf77a-1208">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="bf77a-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bf77a-1209">Az.Relay</span></span>
* <span data-ttu-id="bf77a-1210">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="bf77a-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="bf77a-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1211">Az.Resources</span></span>
* <span data-ttu-id="bf77a-1212">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="bf77a-1213">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="bf77a-1214">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="bf77a-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bf77a-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf77a-1216">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="bf77a-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-1217">Az.Sql</span></span>
* <span data-ttu-id="bf77a-1218">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="bf77a-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf77a-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf77a-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf77a-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf77a-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf77a-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf77a-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bf77a-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf77a-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bf77a-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf77a-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bf77a-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf77a-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="bf77a-1227">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="bf77a-1228">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bf77a-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="bf77a-1229">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="bf77a-1230">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="bf77a-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bf77a-1231">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="bf77a-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bf77a-1232">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="bf77a-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="bf77a-1233">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="bf77a-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="bf77a-1234">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="bf77a-1235">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bf77a-1236">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bf77a-1236">General</span></span>
* <span data-ttu-id="bf77a-1237">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="bf77a-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="bf77a-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1238">Az.Profile</span></span>
* <span data-ttu-id="bf77a-1239">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="bf77a-1240">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="bf77a-1241">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="bf77a-1242">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="bf77a-1243">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="bf77a-1244">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="bf77a-1245">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="bf77a-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf77a-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf77a-1247">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-1248">Az.Compute</span></span>
* <span data-ttu-id="bf77a-1249">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="bf77a-1250">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="bf77a-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="bf77a-1251">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="bf77a-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-1253">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="bf77a-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="bf77a-1254">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="bf77a-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="bf77a-1255">Az.Insights</span></span>
* <span data-ttu-id="bf77a-1256">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="bf77a-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="bf77a-1257">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="bf77a-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="bf77a-1258">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="bf77a-1259">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-1260">Az.Network</span></span>
* <span data-ttu-id="bf77a-1261">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bf77a-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="bf77a-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf77a-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="bf77a-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bf77a-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="bf77a-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bf77a-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="bf77a-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="bf77a-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="bf77a-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf77a-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="bf77a-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bf77a-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf77a-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf77a-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf77a-1269">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1270">Az.Resources</span></span>
* <span data-ttu-id="bf77a-1271">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="bf77a-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="bf77a-1272">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="bf77a-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf77a-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf77a-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="bf77a-1274">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="bf77a-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf77a-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf77a-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf77a-1276">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="bf77a-1277">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bf77a-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="bf77a-1278">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="bf77a-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="bf77a-1279">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="bf77a-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="bf77a-1280">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="bf77a-1281">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="bf77a-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1282">Az.Profile</span></span>
* <span data-ttu-id="bf77a-1283">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="bf77a-1284">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-1285">Az.Compute</span></span>
* <span data-ttu-id="bf77a-1286">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="bf77a-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="bf77a-1287">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf77a-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf77a-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf77a-1289">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="bf77a-1290">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="bf77a-1291">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bf77a-1292">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bf77a-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-1294">Az.Network</span></span>
* <span data-ttu-id="bf77a-1295">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="bf77a-1296">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1297">Az.Resources</span></span>
* <span data-ttu-id="bf77a-1298">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="bf77a-1299">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="bf77a-1300">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="bf77a-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="bf77a-1301">Azure.Storage</span></span>
* <span data-ttu-id="bf77a-1302">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="bf77a-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="bf77a-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf77a-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="bf77a-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bf77a-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bf77a-1305">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="bf77a-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="bf77a-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="bf77a-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf77a-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf77a-1308">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf77a-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf77a-1309">Az.Compute</span></span>
* <span data-ttu-id="bf77a-1310">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="bf77a-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="bf77a-1311">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="bf77a-1312">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="bf77a-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bf77a-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="bf77a-1314">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf77a-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf77a-1315">Az.Network</span></span>
* <span data-ttu-id="bf77a-1316">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="bf77a-1317">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1317">new cmdlets added</span></span>
    - <span data-ttu-id="bf77a-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf77a-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf77a-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf77a-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf77a-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf77a-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="bf77a-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf77a-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="bf77a-1324">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="bf77a-1325">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="bf77a-1326">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bf77a-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bf77a-1327">Az.RedisCache</span></span>
* <span data-ttu-id="bf77a-1328">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="bf77a-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="bf77a-1329">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf77a-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf77a-1330">Az.Resources</span></span>
* <span data-ttu-id="bf77a-1331">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bf77a-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bf77a-1332">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="bf77a-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf77a-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf77a-1333">Az.Sql</span></span>
* <span data-ttu-id="bf77a-1334">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="bf77a-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf77a-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf77a-1335">Az.Websites</span></span>
* <span data-ttu-id="bf77a-1336">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="bf77a-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="bf77a-1337">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="bf77a-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="bf77a-1338">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="bf77a-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="bf77a-1339">Erste Version</span><span class="sxs-lookup"><span data-stu-id="bf77a-1339">Initial Release</span></span>