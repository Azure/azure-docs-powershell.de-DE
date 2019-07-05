---
ms.openlocfilehash: ac8513b3eee4adfcaf0be8bf7b4e8d09190811df
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516639"
---
## <a name="240---july-2019"></a><span data-ttu-id="d05c6-101">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-102">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-103">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d05c6-104">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d05c6-105">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="d05c6-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d05c6-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d05c6-106">Az.Advisor</span></span>
* <span data-ttu-id="d05c6-107">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d05c6-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d05c6-108">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="d05c6-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d05c6-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d05c6-109">Az.ApiManagement</span></span>
* <span data-ttu-id="d05c6-110">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d05c6-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d05c6-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d05c6-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d05c6-112">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d05c6-113">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="d05c6-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d05c6-114">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d05c6-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d05c6-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d05c6-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d05c6-116">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-116">Added support for specifiying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-117">Az.Automation</span></span>
* <span data-ttu-id="d05c6-118">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-119">Az.Compute</span></span>
* <span data-ttu-id="d05c6-120">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d05c6-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d05c6-121">Az.DataFactory</span></span>
* <span data-ttu-id="d05c6-122">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="d05c6-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d05c6-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d05c6-123">Az.EventGrid</span></span>
* <span data-ttu-id="d05c6-124">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d05c6-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-125">Az.IotHub</span></span>
* <span data-ttu-id="d05c6-126">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-127">Az.Network</span></span>
* <span data-ttu-id="d05c6-128">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d05c6-129">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="d05c6-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d05c6-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="d05c6-131">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d05c6-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d05c6-132">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d05c6-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d05c6-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="d05c6-134">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-136">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="d05c6-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-137">Az.Resources</span></span>
    - <span data-ttu-id="d05c6-138">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d05c6-139">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d05c6-140">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d05c6-141">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d05c6-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d05c6-142">Az.ServiceBus</span></span>
* <span data-ttu-id="d05c6-143">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="d05c6-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-144">Az.Sql</span></span>
* <span data-ttu-id="d05c6-145">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d05c6-146">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d05c6-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d05c6-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d05c6-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d05c6-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d05c6-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d05c6-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d05c6-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d05c6-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d05c6-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d05c6-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d05c6-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d05c6-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d05c6-153">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-154">Az.Storage</span></span>
* <span data-ttu-id="d05c6-155">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="d05c6-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d05c6-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d05c6-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d05c6-157">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="d05c6-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d05c6-158">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="d05c6-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d05c6-159">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d05c6-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d05c6-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d05c6-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d05c6-162">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="d05c6-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d05c6-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d05c6-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d05c6-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d05c6-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d05c6-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d05c6-165">Az.StorageSync</span></span>
* <span data-ttu-id="d05c6-166">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="d05c6-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d05c6-167">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-168">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-169">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="d05c6-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d05c6-170">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d05c6-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d05c6-171">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d05c6-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d05c6-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d05c6-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d05c6-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-174">Az.Compute</span></span>
* <span data-ttu-id="d05c6-175">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="d05c6-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d05c6-176">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d05c6-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d05c6-177">Az.Dns</span></span>
* <span data-ttu-id="d05c6-178">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d05c6-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d05c6-179">Az.EventGrid</span></span>
* <span data-ttu-id="d05c6-180">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d05c6-181">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d05c6-181">New cmdlets:</span></span>
    - <span data-ttu-id="d05c6-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d05c6-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d05c6-183">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="d05c6-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d05c6-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d05c6-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d05c6-185">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d05c6-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d05c6-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d05c6-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d05c6-187">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="d05c6-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d05c6-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d05c6-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d05c6-189">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="d05c6-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d05c6-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d05c6-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d05c6-191">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d05c6-192">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d05c6-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d05c6-193">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="d05c6-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d05c6-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d05c6-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d05c6-195">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d05c6-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="d05c6-196">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d05c6-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d05c6-197">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="d05c6-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d05c6-198">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d05c6-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="d05c6-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d05c6-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d05c6-200">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="d05c6-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d05c6-201">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="d05c6-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d05c6-202">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="d05c6-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d05c6-203">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="d05c6-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d05c6-204">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="d05c6-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d05c6-205">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="d05c6-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d05c6-206">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d05c6-207">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="d05c6-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="d05c6-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d05c6-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d05c6-209">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d05c6-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d05c6-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d05c6-211">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="d05c6-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d05c6-212">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="d05c6-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d05c6-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d05c6-213">Az.FrontDoor</span></span>
* <span data-ttu-id="d05c6-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d05c6-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d05c6-215">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d05c6-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d05c6-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d05c6-217">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-218">Az.Network</span></span>
* <span data-ttu-id="d05c6-219">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d05c6-220">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-220">New cmdlets</span></span>
        - <span data-ttu-id="d05c6-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d05c6-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d05c6-222">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d05c6-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d05c6-223">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-223">New cmdlets</span></span> 
        - <span data-ttu-id="d05c6-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d05c6-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d05c6-225">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d05c6-226">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-226">New cmdlets</span></span> 
        - <span data-ttu-id="d05c6-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d05c6-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="d05c6-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d05c6-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d05c6-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d05c6-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d05c6-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d05c6-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d05c6-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d05c6-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d05c6-232">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d05c6-233">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-233">New cmdlets</span></span>
        - <span data-ttu-id="d05c6-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d05c6-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d05c6-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d05c6-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d05c6-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d05c6-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d05c6-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d05c6-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d05c6-238">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="d05c6-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d05c6-239">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="d05c6-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d05c6-240">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="d05c6-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d05c6-241">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d05c6-242">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d05c6-243">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="d05c6-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d05c6-244">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d05c6-245">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="d05c6-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d05c6-246">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d05c6-247">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d05c6-248">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="d05c6-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d05c6-249">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d05c6-250">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d05c6-251">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d05c6-252">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="d05c6-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d05c6-253">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d05c6-254">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d05c6-255">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="d05c6-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d05c6-256">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="d05c6-257">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="d05c6-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="d05c6-258">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d05c6-259">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d05c6-260">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d05c6-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="d05c6-262">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="d05c6-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-263">Az.Resources</span></span>
* <span data-ttu-id="d05c6-264">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d05c6-265">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d05c6-266">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d05c6-267">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="d05c6-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d05c6-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="d05c6-269">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="d05c6-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-270">Az.Sql</span></span>
* <span data-ttu-id="d05c6-271">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d05c6-272">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d05c6-273">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d05c6-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d05c6-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d05c6-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d05c6-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d05c6-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d05c6-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d05c6-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d05c6-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d05c6-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d05c6-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-279">Az.Storage</span></span>
* <span data-ttu-id="d05c6-280">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d05c6-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d05c6-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="d05c6-282">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="d05c6-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d05c6-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d05c6-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-284">Az.Websites</span></span>
* <span data-ttu-id="d05c6-285">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="d05c6-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d05c6-286">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d05c6-287">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d05c6-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d05c6-288">Az.Cdn</span></span>
* <span data-ttu-id="d05c6-289">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-290">Az.Compute</span></span>
* <span data-ttu-id="d05c6-291">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d05c6-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d05c6-292">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d05c6-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d05c6-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-293">Az.EventHub</span></span>
* <span data-ttu-id="d05c6-294">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="d05c6-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d05c6-295">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="d05c6-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-296">Az.Network</span></span>
* <span data-ttu-id="d05c6-297">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d05c6-298">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d05c6-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="d05c6-300">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d05c6-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-302">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="d05c6-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d05c6-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d05c6-303">Az.ServiceBus</span></span>
* <span data-ttu-id="d05c6-304">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="d05c6-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d05c6-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="d05c6-306">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d05c6-307">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-308">Az.Sql</span></span>
* <span data-ttu-id="d05c6-309">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="d05c6-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d05c6-310">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d05c6-311">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="d05c6-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d05c6-312">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="d05c6-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-313">Az.Websites</span></span>
* <span data-ttu-id="d05c6-314">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d05c6-315">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d05c6-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d05c6-316">Az.ApiManagement</span></span>
* <span data-ttu-id="d05c6-317">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d05c6-318">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="d05c6-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d05c6-319">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="d05c6-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d05c6-320">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="d05c6-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d05c6-321">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="d05c6-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d05c6-322">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="d05c6-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d05c6-323">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="d05c6-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d05c6-324">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="d05c6-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d05c6-325">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d05c6-326">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="d05c6-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d05c6-327">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="d05c6-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d05c6-328">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="d05c6-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d05c6-329">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="d05c6-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d05c6-330">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d05c6-331">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="d05c6-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d05c6-332">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="d05c6-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d05c6-333">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="d05c6-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d05c6-334">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="d05c6-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d05c6-335">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="d05c6-336">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="d05c6-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d05c6-337">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d05c6-338">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="d05c6-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d05c6-339">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="d05c6-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d05c6-340">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="d05c6-341">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d05c6-342">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d05c6-343">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="d05c6-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d05c6-344">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d05c6-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d05c6-345">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d05c6-346">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="d05c6-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d05c6-347">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="d05c6-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="d05c6-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d05c6-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d05c6-349">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d05c6-350">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d05c6-351">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="d05c6-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d05c6-352">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="d05c6-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d05c6-353">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="d05c6-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d05c6-354">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="d05c6-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d05c6-355">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="d05c6-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d05c6-356">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="d05c6-357">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="d05c6-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d05c6-358">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="d05c6-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d05c6-359">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="d05c6-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d05c6-360">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="d05c6-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d05c6-361">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d05c6-362">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="d05c6-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d05c6-363">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="d05c6-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="d05c6-364">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="d05c6-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d05c6-365">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d05c6-366">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="d05c6-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d05c6-367">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="d05c6-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d05c6-368">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="d05c6-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d05c6-369">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="d05c6-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d05c6-370">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d05c6-371">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="d05c6-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d05c6-372">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="d05c6-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d05c6-373">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d05c6-374">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="d05c6-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d05c6-375">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="d05c6-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d05c6-376">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d05c6-377">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d05c6-378">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="d05c6-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d05c6-379">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="d05c6-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d05c6-380">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d05c6-381">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="d05c6-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d05c6-382">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="d05c6-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d05c6-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d05c6-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d05c6-384">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="d05c6-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d05c6-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d05c6-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d05c6-386">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d05c6-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d05c6-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d05c6-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d05c6-388">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d05c6-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d05c6-389">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="d05c6-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d05c6-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d05c6-391">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="d05c6-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="d05c6-392">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d05c6-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d05c6-393">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="d05c6-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-394">Az.Automation</span></span>
* <span data-ttu-id="d05c6-395">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d05c6-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d05c6-396">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d05c6-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d05c6-397">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d05c6-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d05c6-398">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="d05c6-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d05c6-399">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d05c6-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d05c6-400">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="d05c6-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d05c6-401">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="d05c6-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-402">Az.Compute</span></span>
* <span data-ttu-id="d05c6-403">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d05c6-404">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-406">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="d05c6-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d05c6-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d05c6-407">Az.Monitor</span></span>
* <span data-ttu-id="d05c6-408">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="d05c6-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-409">Az.Network</span></span>
* <span data-ttu-id="d05c6-410">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d05c6-411">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d05c6-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="d05c6-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d05c6-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d05c6-413">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d05c6-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-414">Az.Resources</span></span>
* <span data-ttu-id="d05c6-415">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-416">Az.Sql</span></span>
* <span data-ttu-id="d05c6-417">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="d05c6-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d05c6-418">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-419">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-420">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="d05c6-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d05c6-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="d05c6-422">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="d05c6-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d05c6-423">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="d05c6-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-424">Az.Compute</span></span>
* <span data-ttu-id="d05c6-425">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="d05c6-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d05c6-426">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d05c6-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d05c6-427">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d05c6-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d05c6-428">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d05c6-429">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="d05c6-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d05c6-430">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="d05c6-431">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="d05c6-431">Breaking changes</span></span>
    - <span data-ttu-id="d05c6-432">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="d05c6-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d05c6-433">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="d05c6-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d05c6-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d05c6-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="d05c6-435">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d05c6-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d05c6-436">Az.Dns</span></span>
* <span data-ttu-id="d05c6-437">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="d05c6-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d05c6-438">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="d05c6-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d05c6-439">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d05c6-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d05c6-440">Az.FrontDoor</span></span>
* <span data-ttu-id="d05c6-441">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d05c6-442">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="d05c6-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d05c6-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d05c6-443">Az.HDInsight</span></span>
* <span data-ttu-id="d05c6-444">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="d05c6-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d05c6-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d05c6-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d05c6-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d05c6-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d05c6-447">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="d05c6-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d05c6-448">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="d05c6-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d05c6-449">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d05c6-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d05c6-450">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d05c6-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d05c6-451">Az.Monitor</span></span>
* <span data-ttu-id="d05c6-452">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="d05c6-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="d05c6-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d05c6-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d05c6-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d05c6-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d05c6-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d05c6-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d05c6-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d05c6-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d05c6-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d05c6-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d05c6-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d05c6-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d05c6-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d05c6-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d05c6-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d05c6-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d05c6-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d05c6-464">[Weitere Informationen](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="d05c6-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d05c6-465">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="d05c6-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-466">Az.Network</span></span>
* <span data-ttu-id="d05c6-467">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d05c6-468">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-468">New cmdlets</span></span>
        - <span data-ttu-id="d05c6-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d05c6-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="d05c6-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d05c6-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d05c6-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d05c6-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d05c6-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d05c6-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d05c6-473">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-473">Updated cmdlets</span></span>
        - <span data-ttu-id="d05c6-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d05c6-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d05c6-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d05c6-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d05c6-476">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d05c6-477">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="d05c6-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d05c6-478">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="d05c6-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d05c6-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="d05c6-480">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="d05c6-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d05c6-481">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d05c6-482">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="d05c6-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-484">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="d05c6-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d05c6-485">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="d05c6-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d05c6-486">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="d05c6-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d05c6-487">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="d05c6-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d05c6-488">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="d05c6-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d05c6-489">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="d05c6-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d05c6-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d05c6-490">Az.Relay</span></span>
* <span data-ttu-id="d05c6-491">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="d05c6-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d05c6-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d05c6-492">Az.ServiceBus</span></span>
* <span data-ttu-id="d05c6-493">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-494">Az.Storage</span></span>
* <span data-ttu-id="d05c6-495">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="d05c6-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d05c6-496">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="d05c6-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d05c6-497">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="d05c6-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d05c6-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="d05c6-499">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="d05c6-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d05c6-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d05c6-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d05c6-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-503">Az.Websites</span></span>
* <span data-ttu-id="d05c6-504">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d05c6-505">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d05c6-506">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d05c6-507">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="d05c6-507">Highlights since the last major release</span></span>
* <span data-ttu-id="d05c6-508">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="d05c6-508">General availability of `Az` module</span></span>
* <span data-ttu-id="d05c6-509">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="d05c6-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d05c6-510">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="d05c6-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d05c6-511">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d05c6-512">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d05c6-513">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d05c6-514">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d05c6-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-515">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-516">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="d05c6-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d05c6-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d05c6-517">Az.Batch</span></span>
* <span data-ttu-id="d05c6-518">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d05c6-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d05c6-519">Az.Cdn</span></span>
* <span data-ttu-id="d05c6-520">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d05c6-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="d05c6-522">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-523">Az.Compute</span></span>
* <span data-ttu-id="d05c6-524">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="d05c6-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d05c6-525">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d05c6-526">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d05c6-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d05c6-527">Az.DataFactory</span></span>
* <span data-ttu-id="d05c6-528">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="d05c6-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-530">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d05c6-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d05c6-531">Az.EventGrid</span></span>
* <span data-ttu-id="d05c6-532">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d05c6-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d05c6-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-533">Az.EventHub</span></span>
* <span data-ttu-id="d05c6-534">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d05c6-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d05c6-535">Az.HDInsight</span></span>
* <span data-ttu-id="d05c6-536">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d05c6-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-537">Az.IotHub</span></span>
* <span data-ttu-id="d05c6-538">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d05c6-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d05c6-539">Az.KeyVault</span></span>
* <span data-ttu-id="d05c6-540">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d05c6-541">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d05c6-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d05c6-542">Az.MachineLearning</span></span>
* <span data-ttu-id="d05c6-543">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d05c6-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d05c6-544">Az.Media</span></span>
* <span data-ttu-id="d05c6-545">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d05c6-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d05c6-546">Az.Monitor</span></span>
  * <span data-ttu-id="d05c6-547">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="d05c6-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d05c6-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d05c6-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d05c6-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d05c6-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d05c6-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d05c6-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d05c6-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d05c6-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d05c6-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d05c6-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d05c6-553">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-554">Az.Network</span></span>
* <span data-ttu-id="d05c6-555">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d05c6-556">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d05c6-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d05c6-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="d05c6-558">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d05c6-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="d05c6-560">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d05c6-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d05c6-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d05c6-562">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-564">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d05c6-565">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d05c6-566">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d05c6-567">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d05c6-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d05c6-568">Az.RedisCache</span></span>
* <span data-ttu-id="d05c6-569">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-570">Az.Resources</span></span>
* <span data-ttu-id="d05c6-571">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-572">Az.Sql</span></span>
* <span data-ttu-id="d05c6-573">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="d05c6-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d05c6-574">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d05c6-575">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="d05c6-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d05c6-576">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d05c6-577">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="d05c6-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d05c6-578">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="d05c6-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d05c6-579">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-580">Az.Websites</span></span>
* <span data-ttu-id="d05c6-581">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="d05c6-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d05c6-582">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d05c6-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d05c6-583">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d05c6-584">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d05c6-585">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d05c6-586">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="d05c6-586">Highlights since the last major release</span></span>
* <span data-ttu-id="d05c6-587">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="d05c6-587">General availability of `Az` module</span></span>
* <span data-ttu-id="d05c6-588">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="d05c6-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d05c6-589">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="d05c6-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d05c6-590">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d05c6-591">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d05c6-592">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d05c6-593">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d05c6-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-594">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-595">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="d05c6-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d05c6-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="d05c6-597">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d05c6-598">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-599">Az.Automation</span></span>
* <span data-ttu-id="d05c6-600">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="d05c6-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d05c6-601">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d05c6-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d05c6-602">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="d05c6-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-603">Az.Compute</span></span>
* <span data-ttu-id="d05c6-604">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d05c6-605">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="d05c6-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d05c6-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="d05c6-607">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="d05c6-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d05c6-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d05c6-608">Az.DataFactory</span></span>
* <span data-ttu-id="d05c6-609">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d05c6-610">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-611">Az.Resources</span></span>
* <span data-ttu-id="d05c6-612">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="d05c6-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d05c6-613">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="d05c6-613">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d05c6-614">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="d05c6-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d05c6-615">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d05c6-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d05c6-616">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="d05c6-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d05c6-617">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d05c6-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-618">Az.Sql</span></span>
* <span data-ttu-id="d05c6-619">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="d05c6-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-620">Az.Storage</span></span>
* <span data-ttu-id="d05c6-621">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="d05c6-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d05c6-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d05c6-622">New-AzStorageContext</span></span>
* <span data-ttu-id="d05c6-623">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="d05c6-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d05c6-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d05c6-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d05c6-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d05c6-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d05c6-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d05c6-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d05c6-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d05c6-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d05c6-628">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="d05c6-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d05c6-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d05c6-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d05c6-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d05c6-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d05c6-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d05c6-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d05c6-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d05c6-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d05c6-633">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d05c6-634">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="d05c6-634">Highlights since the last major release</span></span>
* <span data-ttu-id="d05c6-635">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="d05c6-635">General availability of `Az` module</span></span>
* <span data-ttu-id="d05c6-636">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="d05c6-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d05c6-637">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="d05c6-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d05c6-638">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d05c6-639">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d05c6-640">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d05c6-641">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-642">Az.Automation</span></span>
* <span data-ttu-id="d05c6-643">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="d05c6-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d05c6-644">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="d05c6-644">Dynamic grouping</span></span>
    * <span data-ttu-id="d05c6-645">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="d05c6-645">Pre-Post script</span></span>
    * <span data-ttu-id="d05c6-646">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="d05c6-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-647">Az.Compute</span></span>
* <span data-ttu-id="d05c6-648">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d05c6-649">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d05c6-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d05c6-650">Az.KeyVault</span></span>
* <span data-ttu-id="d05c6-651">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-652">Az.Network</span></span>
* <span data-ttu-id="d05c6-653">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d05c6-654">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-656">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="d05c6-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d05c6-657">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-658">Az.Resources</span></span>
* <span data-ttu-id="d05c6-659">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d05c6-660">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d05c6-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-661">Az.Sql</span></span>
* <span data-ttu-id="d05c6-662">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-663">Az.Storage</span></span>
* <span data-ttu-id="d05c6-664">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d05c6-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d05c6-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d05c6-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d05c6-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d05c6-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d05c6-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d05c6-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d05c6-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d05c6-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d05c6-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d05c6-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-671">Az.Websites</span></span>
* <span data-ttu-id="d05c6-672">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="d05c6-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d05c6-673">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-674">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-675">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d05c6-676">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-677">Az.Automation</span></span>
* <span data-ttu-id="d05c6-678">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="d05c6-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d05c6-679">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d05c6-680">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d05c6-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d05c6-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d05c6-681">Az.Cdn</span></span>
* <span data-ttu-id="d05c6-682">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="d05c6-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-683">Az.Compute</span></span>
* <span data-ttu-id="d05c6-684">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d05c6-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d05c6-685">Az.DataFactory</span></span>
* <span data-ttu-id="d05c6-686">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d05c6-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d05c6-687">Az.LogicApp</span></span>
* <span data-ttu-id="d05c6-688">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d05c6-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-689">Az.Network</span></span>
* <span data-ttu-id="d05c6-690">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-692">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="d05c6-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d05c6-693">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="d05c6-693">SDK Update</span></span>
* <span data-ttu-id="d05c6-694">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d05c6-695">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-696">Az.Resources</span></span>
* <span data-ttu-id="d05c6-697">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d05c6-698">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d05c6-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d05c6-699">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d05c6-700">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d05c6-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d05c6-701">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d05c6-702">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d05c6-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-703">Az.Sql</span></span>
* <span data-ttu-id="d05c6-704">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d05c6-705">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-706">Az.Storage</span></span>
* <span data-ttu-id="d05c6-707">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d05c6-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d05c6-708">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d05c6-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="d05c6-710">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-711">Az.Automation</span></span>
* <span data-ttu-id="d05c6-712">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d05c6-713">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d05c6-714">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="d05c6-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d05c6-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="d05c6-716">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d05c6-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-717">Az.Compute</span></span>
* <span data-ttu-id="d05c6-718">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d05c6-719">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="d05c6-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d05c6-720">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d05c6-721">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="d05c6-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-723">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d05c6-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-724">Az.EventHub</span></span>
* <span data-ttu-id="d05c6-725">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d05c6-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d05c6-726">Az.KeyVault</span></span>
* <span data-ttu-id="d05c6-727">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d05c6-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d05c6-728">Az.LogicApp</span></span>
* <span data-ttu-id="d05c6-729">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d05c6-730">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d05c6-731">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="d05c6-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d05c6-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d05c6-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d05c6-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d05c6-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d05c6-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d05c6-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d05c6-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d05c6-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d05c6-736">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d05c6-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d05c6-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d05c6-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d05c6-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d05c6-741">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d05c6-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d05c6-742">Az.Monitor</span></span>
* <span data-ttu-id="d05c6-743">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-744">Az.Network</span></span>
* <span data-ttu-id="d05c6-745">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d05c6-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="d05c6-747">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d05c6-748">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d05c6-749">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="d05c6-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d05c6-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-750">Az.Resources</span></span>
* <span data-ttu-id="d05c6-751">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d05c6-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d05c6-752">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d05c6-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d05c6-753">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d05c6-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d05c6-754">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="d05c6-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-755">Az.Sql</span></span>
* <span data-ttu-id="d05c6-756">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d05c6-757">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="d05c6-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-758">Az.Websites</span></span>
* <span data-ttu-id="d05c6-759">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d05c6-760">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-761">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-762">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="d05c6-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d05c6-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-763">Az.AnalysisServices</span></span>
<span data-ttu-id="d05c6-764">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="d05c6-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-765">Az.Compute</span></span>
* <span data-ttu-id="d05c6-766">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d05c6-767">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d05c6-768">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-769">Az.RecoveryServices</span></span>
<span data-ttu-id="d05c6-770">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="d05c6-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-771">Az.Resources</span></span>
* <span data-ttu-id="d05c6-772">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d05c6-773">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d05c6-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d05c6-774">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d05c6-775">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d05c6-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-776">Az.Sql</span></span>
* <span data-ttu-id="d05c6-777">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d05c6-778">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="d05c6-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d05c6-779">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d05c6-780">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-781">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-782">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d05c6-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d05c6-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="d05c6-784">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="d05c6-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="d05c6-786">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="d05c6-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d05c6-787">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-788">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-789">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d05c6-790">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d05c6-791">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d05c6-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d05c6-792">Az.Aks</span></span>
* <span data-ttu-id="d05c6-793">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d05c6-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-794">Az.Automation</span></span>
* <span data-ttu-id="d05c6-795">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d05c6-796">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d05c6-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d05c6-797">Az.Cdn</span></span>
* <span data-ttu-id="d05c6-798">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-799">Az.Compute</span></span>
* <span data-ttu-id="d05c6-800">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d05c6-801">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d05c6-802">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d05c6-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d05c6-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d05c6-804">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d05c6-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d05c6-805">Az.DataFactory</span></span>
* <span data-ttu-id="d05c6-806">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-808">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d05c6-809">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d05c6-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d05c6-810">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d05c6-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-811">Az.IotHub</span></span>
* <span data-ttu-id="d05c6-812">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d05c6-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d05c6-813">Az.KeyVault</span></span>
* <span data-ttu-id="d05c6-814">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-815">Az.Network</span></span>
* <span data-ttu-id="d05c6-816">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-817">Az.Resources</span></span>
* <span data-ttu-id="d05c6-818">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d05c6-819">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="d05c6-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d05c6-820">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="d05c6-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d05c6-821">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d05c6-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d05c6-822">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d05c6-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d05c6-823">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d05c6-824">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d05c6-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d05c6-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="d05c6-826">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="d05c6-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d05c6-827">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-827">Fix some error messages.</span></span>
* <span data-ttu-id="d05c6-828">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="d05c6-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d05c6-829">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="d05c6-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d05c6-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d05c6-830">Az.SignalR</span></span>
* <span data-ttu-id="d05c6-831">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-832">Az.Sql</span></span>
* <span data-ttu-id="d05c6-833">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d05c6-834">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d05c6-835">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="d05c6-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d05c6-836">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="d05c6-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-837">Az.Storage</span></span>
* <span data-ttu-id="d05c6-838">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d05c6-839">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d05c6-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d05c6-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d05c6-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d05c6-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d05c6-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d05c6-842">Az.TrafficManager</span></span>
* <span data-ttu-id="d05c6-843">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-844">Az.Websites</span></span>
* <span data-ttu-id="d05c6-845">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d05c6-846">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="d05c6-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d05c6-847">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d05c6-848">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="d05c6-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d05c6-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-849">Az.Accounts</span></span>
* <span data-ttu-id="d05c6-850">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-851">Az.Compute</span></span>
* <span data-ttu-id="d05c6-852">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="d05c6-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d05c6-853">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d05c6-854">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-856">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d05c6-857">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d05c6-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d05c6-858">Az.EventGrid</span></span>
* <span data-ttu-id="d05c6-859">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d05c6-860">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d05c6-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d05c6-861">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="d05c6-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d05c6-862">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d05c6-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d05c6-863">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d05c6-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d05c6-864">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d05c6-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d05c6-865">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="d05c6-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d05c6-866">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d05c6-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d05c6-867">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d05c6-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d05c6-868">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d05c6-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="d05c6-869">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d05c6-870">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="d05c6-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d05c6-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d05c6-871">Az.IotHub</span></span>
* <span data-ttu-id="d05c6-872">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d05c6-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d05c6-873">Az.LogicApp</span></span>
* <span data-ttu-id="d05c6-874">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="d05c6-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-875">Az.Resources</span></span>
* <span data-ttu-id="d05c6-876">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d05c6-877">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d05c6-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d05c6-878">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d05c6-879">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d05c6-880">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="d05c6-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d05c6-881">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d05c6-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d05c6-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d05c6-882">Az.SignalR</span></span>
* <span data-ttu-id="d05c6-883">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-884">Az.Sql</span></span>
* <span data-ttu-id="d05c6-885">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d05c6-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-886">Az.Storage</span></span>
* <span data-ttu-id="d05c6-887">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d05c6-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d05c6-888">New-AzStorageContext</span></span>
* <span data-ttu-id="d05c6-889">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="d05c6-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d05c6-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d05c6-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-891">Az.Websites</span></span>
* <span data-ttu-id="d05c6-892">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d05c6-893">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d05c6-894">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d05c6-895">Allgemein</span><span class="sxs-lookup"><span data-stu-id="d05c6-895">General</span></span>

- <span data-ttu-id="d05c6-896">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="d05c6-896">General Availability of Az Module</span></span>
- <span data-ttu-id="d05c6-897">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="d05c6-897">Online help for each module</span></span>
- <span data-ttu-id="d05c6-898">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="d05c6-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d05c6-899">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d05c6-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d05c6-900">Az.Accounts</span></span>
- <span data-ttu-id="d05c6-901">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d05c6-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="d05c6-902">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="d05c6-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d05c6-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d05c6-903">Az.ApiManagement</span></span>
- <span data-ttu-id="d05c6-904">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="d05c6-904">Fixes for #7002</span></span>
- <span data-ttu-id="d05c6-905">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d05c6-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d05c6-906">Az.Batch</span></span>
- <span data-ttu-id="d05c6-907">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d05c6-908">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="d05c6-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d05c6-909">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d05c6-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d05c6-910">Az.Billing</span></span>
- <span data-ttu-id="d05c6-911">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d05c6-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-912">Az.CognitivServices</span></span>
- <span data-ttu-id="d05c6-913">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d05c6-914">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d05c6-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="d05c6-916">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d05c6-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d05c6-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d05c6-918">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="d05c6-920">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d05c6-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d05c6-921">Az.Monitor</span></span>
- <span data-ttu-id="d05c6-922">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d05c6-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d05c6-923">Az.KeyVault</span></span>
- <span data-ttu-id="d05c6-924">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d05c6-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d05c6-925">Az.MachineLearning</span></span>
- <span data-ttu-id="d05c6-926">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="d05c6-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d05c6-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d05c6-927">Az.Media</span></span>
- <span data-ttu-id="d05c6-928">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="d05c6-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d05c6-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-929">Az.Network</span></span>
<span data-ttu-id="d05c6-930">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d05c6-931">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d05c6-931">New cmdlets added:</span></span>
        - <span data-ttu-id="d05c6-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d05c6-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d05c6-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d05c6-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d05c6-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d05c6-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d05c6-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d05c6-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d05c6-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d05c6-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d05c6-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d05c6-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d05c6-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d05c6-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05c6-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d05c6-940">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d05c6-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d05c6-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d05c6-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d05c6-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d05c6-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d05c6-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d05c6-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d05c6-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d05c6-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d05c6-946">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d05c6-947">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d05c6-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d05c6-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d05c6-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d05c6-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d05c6-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d05c6-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d05c6-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d05c6-951">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d05c6-952">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d05c6-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="d05c6-954">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d05c6-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d05c6-955">Az.Profile</span></span>
- <span data-ttu-id="d05c6-956">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="d05c6-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="d05c6-958">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d05c6-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-959">Az.Resources</span></span>
- <span data-ttu-id="d05c6-960">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d05c6-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="d05c6-962">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="d05c6-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d05c6-963">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d05c6-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d05c6-964">Az.SIgnalR</span></span>
- <span data-ttu-id="d05c6-965">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d05c6-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d05c6-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-966">Az.Sql</span></span>
- <span data-ttu-id="d05c6-967">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d05c6-968">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d05c6-969">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d05c6-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-970">Az.Storage</span></span>
- <span data-ttu-id="d05c6-971">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d05c6-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-972">Az.Websites</span></span>
- <span data-ttu-id="d05c6-973">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d05c6-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d05c6-974">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d05c6-975">Allgemein</span><span class="sxs-lookup"><span data-stu-id="d05c6-975">General</span></span>

* <span data-ttu-id="d05c6-976">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="d05c6-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d05c6-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-977">Az.Compute</span></span>

* <span data-ttu-id="d05c6-978">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="d05c6-980">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d05c6-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d05c6-981">Az.FrontDoor</span></span>

* <span data-ttu-id="d05c6-982">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-982">Fixed some broken links</span></span>
    - <span data-ttu-id="d05c6-983">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d05c6-984">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d05c6-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="d05c6-986">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d05c6-987">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="d05c6-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d05c6-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-988">Az.Resources</span></span>

* <span data-ttu-id="d05c6-989">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="d05c6-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d05c6-990">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d05c6-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d05c6-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-991">Az.Sql</span></span>

* <span data-ttu-id="d05c6-992">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="d05c6-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d05c6-993">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d05c6-994">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d05c6-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-995">Az.Storage</span></span>

* <span data-ttu-id="d05c6-996">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d05c6-997">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d05c6-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d05c6-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d05c6-999">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="d05c6-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d05c6-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d05c6-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d05c6-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d05c6-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-1002">Az.Websites</span></span>

* <span data-ttu-id="d05c6-1003">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d05c6-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d05c6-1004">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d05c6-1005">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d05c6-1006">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d05c6-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d05c6-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="d05c6-1008">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d05c6-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d05c6-1009">Az.Automation</span></span>
* <span data-ttu-id="d05c6-1010">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d05c6-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d05c6-1011">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d05c6-1012">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d05c6-1013">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d05c6-1014">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d05c6-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-1015">Az.Compute</span></span>
* <span data-ttu-id="d05c6-1016">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d05c6-1017">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d05c6-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="d05c6-1019">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d05c6-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d05c6-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d05c6-1021">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d05c6-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-1022">Az.Network</span></span>
* <span data-ttu-id="d05c6-1023">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d05c6-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d05c6-1024">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d05c6-1025">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d05c6-1026">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d05c6-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d05c6-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d05c6-1028">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d05c6-1029">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d05c6-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d05c6-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d05c6-1031">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="d05c6-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d05c6-1032">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d05c6-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d05c6-1033">Az.Relay</span></span>
* <span data-ttu-id="d05c6-1034">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="d05c6-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d05c6-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-1035">Az.Resources</span></span>
* <span data-ttu-id="d05c6-1036">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d05c6-1037">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d05c6-1038">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d05c6-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d05c6-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="d05c6-1040">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d05c6-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-1041">Az.Sql</span></span>
* <span data-ttu-id="d05c6-1042">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d05c6-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d05c6-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d05c6-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d05c6-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d05c6-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d05c6-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d05c6-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d05c6-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d05c6-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d05c6-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d05c6-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d05c6-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d05c6-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d05c6-1051">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d05c6-1052">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="d05c6-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d05c6-1053">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d05c6-1054">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="d05c6-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d05c6-1055">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="d05c6-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d05c6-1056">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d05c6-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d05c6-1057">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d05c6-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d05c6-1058">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d05c6-1059">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d05c6-1060">Allgemein</span><span class="sxs-lookup"><span data-stu-id="d05c6-1060">General</span></span>
* <span data-ttu-id="d05c6-1061">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="d05c6-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d05c6-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d05c6-1062">Az.Profile</span></span>
* <span data-ttu-id="d05c6-1063">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d05c6-1064">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d05c6-1065">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d05c6-1066">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d05c6-1067">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d05c6-1068">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d05c6-1069">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="d05c6-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d05c6-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="d05c6-1071">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-1072">Az.Compute</span></span>
* <span data-ttu-id="d05c6-1073">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d05c6-1074">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="d05c6-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d05c6-1075">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="d05c6-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-1077">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="d05c6-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d05c6-1078">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d05c6-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d05c6-1079">Az.Insights</span></span>
* <span data-ttu-id="d05c6-1080">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="d05c6-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d05c6-1081">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="d05c6-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d05c6-1082">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d05c6-1083">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-1084">Az.Network</span></span>
* <span data-ttu-id="d05c6-1085">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d05c6-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d05c6-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d05c6-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d05c6-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d05c6-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d05c6-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d05c6-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d05c6-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d05c6-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d05c6-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d05c6-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d05c6-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d05c6-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d05c6-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d05c6-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="d05c6-1093">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-1094">Az.Resources</span></span>
* <span data-ttu-id="d05c6-1095">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="d05c6-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d05c6-1096">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="d05c6-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d05c6-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d05c6-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="d05c6-1098">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="d05c6-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d05c6-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d05c6-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="d05c6-1100">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d05c6-1101">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="d05c6-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d05c6-1102">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="d05c6-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d05c6-1103">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="d05c6-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d05c6-1104">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d05c6-1105">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d05c6-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d05c6-1106">Az.Profile</span></span>
* <span data-ttu-id="d05c6-1107">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d05c6-1108">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-1109">Az.Compute</span></span>
* <span data-ttu-id="d05c6-1110">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="d05c6-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d05c6-1111">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d05c6-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d05c6-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="d05c6-1113">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d05c6-1114">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d05c6-1115">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d05c6-1116">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d05c6-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-1118">Az.Network</span></span>
* <span data-ttu-id="d05c6-1119">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d05c6-1120">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-1121">Az.Resources</span></span>
* <span data-ttu-id="d05c6-1122">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d05c6-1123">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d05c6-1124">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d05c6-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d05c6-1125">Azure.Storage</span></span>
* <span data-ttu-id="d05c6-1126">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="d05c6-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d05c6-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d05c6-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d05c6-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d05c6-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d05c6-1129">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d05c6-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d05c6-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d05c6-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d05c6-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="d05c6-1132">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d05c6-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d05c6-1133">Az.Compute</span></span>
* <span data-ttu-id="d05c6-1134">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="d05c6-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d05c6-1135">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d05c6-1136">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d05c6-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d05c6-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d05c6-1138">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d05c6-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d05c6-1139">Az.Network</span></span>
* <span data-ttu-id="d05c6-1140">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d05c6-1141">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1141">new cmdlets added</span></span>
    - <span data-ttu-id="d05c6-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d05c6-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d05c6-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d05c6-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d05c6-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d05c6-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d05c6-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d05c6-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d05c6-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d05c6-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d05c6-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d05c6-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d05c6-1148">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d05c6-1149">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d05c6-1150">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d05c6-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d05c6-1151">Az.RedisCache</span></span>
* <span data-ttu-id="d05c6-1152">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="d05c6-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d05c6-1153">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d05c6-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d05c6-1154">Az.Resources</span></span>
* <span data-ttu-id="d05c6-1155">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d05c6-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d05c6-1156">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="d05c6-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d05c6-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d05c6-1157">Az.Sql</span></span>
* <span data-ttu-id="d05c6-1158">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="d05c6-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d05c6-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d05c6-1159">Az.Websites</span></span>
* <span data-ttu-id="d05c6-1160">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="d05c6-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d05c6-1161">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="d05c6-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d05c6-1162">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="d05c6-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d05c6-1163">Erste Version</span><span class="sxs-lookup"><span data-stu-id="d05c6-1163">Initial Release</span></span>