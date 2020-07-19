---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382179"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7fd76-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fd76-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="7fd76-104">4.4.0 – Juli 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-105">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-106">Neues Cmdlet „Invoke-AzRestMethod“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="7fd76-107">Ein Problem wurde behoben, das Authentifizierungsfehler in Szenarien mit mehreren Prozessen verursachen konnte, z. B. beim Ausführen mehrerer Azure PowerShell-Cmdlets mithilfe von „Start-Job“ [Nr. 9448].</span><span class="sxs-lookup"><span data-stu-id="7fd76-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="7fd76-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7fd76-108">Az.Aks</span></span>
* <span data-ttu-id="7fd76-109">Fehler behoben: „Get-AzAks“ ruft nicht alle Cluster ab [Nr. 12296]</span><span class="sxs-lookup"><span data-stu-id="7fd76-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fd76-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fd76-111">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-112">Az.Automation</span></span>
* <span data-ttu-id="7fd76-113">Das Problem wurde behoben, dass die Zeichenfolge mit Escapezeichen nicht in das JSON-Objekt konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fd76-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-114">Az.Compute</span></span>
* <span data-ttu-id="7fd76-115">Beim Verwenden von „New-azvmss“ ohne die Imageversion „latest“ wurde eine Warnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-116">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-117">Globale Parameter zu Data Factory hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fd76-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fd76-118">Az.EventGrid</span></span>
* <span data-ttu-id="7fd76-119">Zur Verwendung der API-Version 2020-06-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="7fd76-120">Neue Funktionen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-120">Added new features:</span></span>
    - <span data-ttu-id="7fd76-121">Eingabezuordnung</span><span class="sxs-lookup"><span data-stu-id="7fd76-121">Input mapping</span></span>
    - <span data-ttu-id="7fd76-122">Schema für Ereignisbereitstellung</span><span class="sxs-lookup"><span data-stu-id="7fd76-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="7fd76-123">Private Link</span><span class="sxs-lookup"><span data-stu-id="7fd76-123">Private Link</span></span>
    - <span data-ttu-id="7fd76-124">Cloud Event V10-Schema</span><span class="sxs-lookup"><span data-stu-id="7fd76-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="7fd76-125">Service Bus-Thema as Ziel</span><span class="sxs-lookup"><span data-stu-id="7fd76-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="7fd76-126">Azure-Funktion als Ziel</span><span class="sxs-lookup"><span data-stu-id="7fd76-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="7fd76-127">WebHook-Batchverarbeitung</span><span class="sxs-lookup"><span data-stu-id="7fd76-127">WebHook Batching</span></span>
    - <span data-ttu-id="7fd76-128">Sicherer Webhook (AAD-Unterstützung)</span><span class="sxs-lookup"><span data-stu-id="7fd76-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="7fd76-129">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="7fd76-129">IpFiltering</span></span>
* <span data-ttu-id="7fd76-130">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="7fd76-131">„New-AzEventGridSubscription“/„Update-AzEventGridSubscription“:</span><span class="sxs-lookup"><span data-stu-id="7fd76-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="7fd76-132">Neue optionale Parameter zur Unterstützung der Webhook-Batchverarbeitung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="7fd76-133">Neue optionale Parameter zur Unterstützung der Batchverarbeitung gesicherter Webhooks mithilfe von AAD hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="7fd76-134">Neue Enumeration für den EndpointType-Parameter hinzufügen, um das Azure-Funktions-und Service Bus-Thema als neue Ziele zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="7fd76-135">Neuen optionalen Parameter für das Zustellungsschema hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="7fd76-136">„New-AzEventGridTopic“/„Update-AzEventGridTopic“ und „New-AzEventGridDomain“/„Update-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="7fd76-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="7fd76-137">Neue optionale Parameter zur Unterstützung von IpFiltering hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="7fd76-138">„New-AzEventGridTopic“/„New-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="7fd76-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="7fd76-139">Neue optionale Parameter zur Unterstützung von Eingabezuordnung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-140">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-141">Modul zur Verwendung von API 2020-05-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="7fd76-142">Unterstützung für private Links für Storage-, Keyvault- und Web App Service-Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-143">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-144">Erstellen eines Clusters mit ADLSGen1/2-Speicher in nationalen Clouds unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-145">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-146">Fehler für „Get-AzDiagnosticSetting“ behoben, wenn Metriken oder Protokolle NULL sind [Nr. 12272]</span><span class="sxs-lookup"><span data-stu-id="7fd76-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-147">Az.Network</span></span>
* <span data-ttu-id="7fd76-148">Austausch von Parametern in VWan-HubVnet-Verbindung-korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="7fd76-149">Neue Cmdlets für Sites von virtuellen Azure-Netzwerkgeräten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="7fd76-150">„Get-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="7fd76-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7fd76-151">„New-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="7fd76-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7fd76-152">„Remove-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="7fd76-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7fd76-153">„Update-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="7fd76-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7fd76-154">„New-AzOffice365PolicyProperty“</span><span class="sxs-lookup"><span data-stu-id="7fd76-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="7fd76-155">Neue Cmdlets für virtuelle Azure-Netzwerkgeräte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="7fd76-156">„Get-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="7fd76-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7fd76-157">„New-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="7fd76-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7fd76-158">„Remove-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="7fd76-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7fd76-159">„Update-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="7fd76-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7fd76-160">„Get-AzNetworkVirtualApplianceSku“</span><span class="sxs-lookup"><span data-stu-id="7fd76-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="7fd76-161">„New-AzVirtualApplianceSkuProperty“</span><span class="sxs-lookup"><span data-stu-id="7fd76-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="7fd76-162">Onboarding für Application Gateway für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="7fd76-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="7fd76-163">Onboarding für StorageSync für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="7fd76-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="7fd76-164">Onboarding für SignalR für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="7fd76-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-166">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="7fd76-167">Azure Backup hat Cmdlets optimiert, um den Text genauer zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="7fd76-168">Azure Backup hat Unterstützung für das Abrufen von MAB-Agent-Aufträgen mithilfe des Cmdlets „Get-AzRecoveryServicesBackupJob“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-169">Az.Resources</span></span>
* <span data-ttu-id="7fd76-170">„Save-azresourcegroupdeploymenttemplate“ auf Verwendung des SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="7fd76-171">Cmdlet „Unregister-AzResourceProvider“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-172">Az.Sql</span></span>
* <span data-ttu-id="7fd76-173">Unterstützung für Dienstprinzipal und Gastbenutzer im Cmdlet „Set-AzSqlInstanceActiveDirectoryAdministrator“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="7fd76-174">Problem in Data Classification-Cmdlets behoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="7fd76-175">Unterstützung für Azure SQL Managed Instance-Failover hinzugefügt: „Invoke-AzSqlInstanceFailover“</span><span class="sxs-lookup"><span data-stu-id="7fd76-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-176">Az.Storage</span></span>
* <span data-ttu-id="7fd76-177">Problem behoben, dass UserAgent für einige Datenebenen-Cmdlets nicht hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd76-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="7fd76-178">Erstellen/Aktualisieren eines Storage-Kontos mit „MinimumTlsVersion“ und „AllowBlobPublicAccess“ unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fd76-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="7fd76-179">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="7fd76-180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7fd76-181">Aktivieren/Deaktivieren der Versionsverwaltung für Blobdienst eines Storage-Kontos unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="7fd76-182">„Update-AzStorageBlobServiceProperty“</span><span class="sxs-lookup"><span data-stu-id="7fd76-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="7fd76-183">Auflisten von Blobs mit Blobversionen unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="7fd76-184">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="7fd76-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="7fd76-185">Abrufen/Entfernen einer einzelnen Blob-Momentaufnahme oder Blobversion unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="7fd76-186">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="7fd76-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="7fd76-187">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="7fd76-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="7fd76-188">Pipeline aus Blobobjekt unterstützen, das aus Azure.Storage.Blobs V12 generiert wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="7fd76-189">„Get-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="7fd76-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="7fd76-190">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="7fd76-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="7fd76-191">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="7fd76-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="7fd76-192">„Set-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="7fd76-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="7fd76-193">„Start-AzStorageBlobCopy“</span><span class="sxs-lookup"><span data-stu-id="7fd76-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7fd76-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7fd76-194">Az.StorageSync</span></span>
* <span data-ttu-id="7fd76-195">Neue Version von StorageSync SDK für ApiVersion 2020-03-01 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="7fd76-196">Cmdlet „Update Storage Sync Service“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="7fd76-197">„Set-AzStorageSyncService“</span><span class="sxs-lookup"><span data-stu-id="7fd76-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="7fd76-198">„IncomingTrafficPolicy“ und „PrivateEndpointConnections“ zu StorageSyncService-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-199">Az.Websites</span></span>
* <span data-ttu-id="7fd76-200">Unterstützung zur Durchführung von Vorgängen für Slots hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="7fd76-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="7fd76-201">4.3.0 – Juni 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-202">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-203">Standardmäßige Unterstützung der Einstellung der Erkennungsumgebung und das Hinzufügen der Umgebung über „Add-AzEnvironment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="7fd76-204">Aktualisieren von vorgeladenen Assemblys [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="7fd76-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="7fd76-205">Assembly „Azure.Core“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="7fd76-206">Fehler behoben, der dazu führen konnte, dass „Connect-AzAccount“ in der Multithread-Ausführung fehlschlägt [#11201]</span><span class="sxs-lookup"><span data-stu-id="7fd76-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="7fd76-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7fd76-207">Az.Aks</span></span>
* <span data-ttu-id="7fd76-208">Ersetzen der Verwendung der alten [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) durch Aufrufe der [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials)- und [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)-APIs</span><span class="sxs-lookup"><span data-stu-id="7fd76-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-209">Az.Batch</span></span>
* <span data-ttu-id="7fd76-210">Az.Batch für die Verwendung der Microsoft.Azure.Management.Batch-SDK-Version auf 11.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="7fd76-211">Möglichkeit zum Festlegen der BatchAccount-Identität im Cmdlet „New-AzBatchAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-213">Anzeige von Kontofunktionen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="7fd76-214">Ändern von PublicNetworkAccess wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-215">Az.Compute</span></span>
* <span data-ttu-id="7fd76-216">Parameter „SimulateEviction“ wurde den Cmdlets „Set-AzVM“ und „Set-AzVmssVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="7fd76-217">„Premium_LRS“ wurde zur Argumentvervollständigung des StorageAccountType-Parameters für das Cmdlet „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="7fd76-218">Unterstatus zu VMCustomScriptExtension hinzugefügt [#11297]</span><span class="sxs-lookup"><span data-stu-id="7fd76-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="7fd76-219">„Delete“ wurde zur Argumentvervollständigung des EvictionPolicy-Parameters für die Cmdlets „New-AzVM“ und „New-AzVMConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="7fd76-220">Name der neuen VM-Erweiterung für SAP korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-221">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-222">ADF .Net-SDK-Version auf 4.9.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-223">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-224">Parameter der verwalteten Identität zu Cmdlets „New-AzEventHubNamespace“ und „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="7fd76-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7fd76-225">Az.Functions</span></span>
* <span data-ttu-id="7fd76-226">Unterstützung zum Erstellen von PowerShell 7.0- und Java 11-Funktions-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-227">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-228">Listenhosts unterstützt und bestimmte Hosts des HDInsight-Clusters neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7fd76-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7fd76-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="7fd76-230">SDK-Version auf 1.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="7fd76-231">Unterstützung für Exporteinstellungen und verwaltete Identität hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-232">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-233">Eingabeobjektparameter für „Set-AzActivityLogAlert“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="7fd76-234">InputObject-Parameter für „Set-AzActionGroup“ korrigiert [#10868]</span><span class="sxs-lookup"><span data-stu-id="7fd76-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-235">Az.Network</span></span>
* <span data-ttu-id="7fd76-236">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="7fd76-237">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="7fd76-238">„New-AzFirewallPolicyDnsSetting“</span><span class="sxs-lookup"><span data-stu-id="7fd76-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="7fd76-239">Unterstützung für Ziel-FQDN in Netzwerkregeln für Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="7fd76-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="7fd76-240">Unterstützung für Back-End-Adresspool-Vorgänge hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="7fd76-241">„New-AzLoadBalancerBackendAddressConfig“</span><span class="sxs-lookup"><span data-stu-id="7fd76-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="7fd76-242">„New-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="7fd76-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="7fd76-243">„Set-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="7fd76-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="7fd76-244">„Remove-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="7fd76-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="7fd76-245">„Get-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="7fd76-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="7fd76-246">Namensvalidierung für „New-AzIpGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="7fd76-247">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="7fd76-248">„New-AzFirewallPolicyThreatIntelWhitelist“</span><span class="sxs-lookup"><span data-stu-id="7fd76-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="7fd76-249">Folgende Befehle für das Feature aktualisiert: Festlegen/Entfernen von benutzerdefinierten DNS-Servern auf „VirtualWan P2SVpnGateway“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="7fd76-250">„New-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="7fd76-251">„Update-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="7fd76-252">„Update-AzVpnGateway“ aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="7fd76-253">Der optionale Parameter „-BgpPeeringAddress“ wurde hinzugefügt, damit Kunden ihre benutzerdefinierten BGSs angeben können, die auf „VpnGateway“ festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="7fd76-254">Neues Cmdlet hinzugefügt, um das Zurücksetzen des Routingstatus einer VirtualHub-Ressource zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="7fd76-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="7fd76-255">„Reset-AzHubRouter“</span><span class="sxs-lookup"><span data-stu-id="7fd76-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="7fd76-256">Folgendes wurde basierend auf der aktuellen Swagger-Änderung für die Firewallrichtlinie aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="7fd76-257">Namen für „RuleGroup“, „RuleCollectionGroup“ und „RuleType“ geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="7fd76-258">Unterstützung für NAT-Regelsammlungen der Firewallrichtlinie zur Unterstützung mehrerer NAT-Regelsammlungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="7fd76-259">[Breaking Change] Obligatorischer Parameter „SourceIpGroup“ für „New-AzFirewallPolicyApplicationRule“ und „New-AzFirewallPolicyNetworkRule“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="7fd76-260">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="7fd76-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="7fd76-261">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="7fd76-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="7fd76-262">[Breaking Change] Obligatorische Parameter entfernt: „TranslatedAddress“, „TranslatedPort“ für „New-AzFirewallPolicyNatRuleCollection“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="7fd76-263">Neue Cmdlets zur Unterstützung von „PrivateLink“ auf Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="7fd76-264">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="7fd76-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7fd76-265">„Get-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="7fd76-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7fd76-266">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="7fd76-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7fd76-267">„Set-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="7fd76-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7fd76-268">„Remove-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="7fd76-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7fd76-269">„New-AzApplicationGatewayPrivateLinkIpConfiguration“</span><span class="sxs-lookup"><span data-stu-id="7fd76-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="7fd76-270">Neue Cmdlets für untergeordnete Ressource „HubRouteTables“ von „VirtualHub“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="7fd76-271">„New-AzVHubRoute“</span><span class="sxs-lookup"><span data-stu-id="7fd76-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="7fd76-272">„New-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="7fd76-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="7fd76-273">„Get-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="7fd76-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="7fd76-274">„Update-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="7fd76-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="7fd76-275">„Remove-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="7fd76-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="7fd76-276">Vorhandene Cmdlets aktualisiert, sodass sie den optionalen Eingabeparameter „RoutingConfiguration“ für benutzerdefiniertes Routing in „VirtualWan“ unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="7fd76-277">„New-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="7fd76-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="7fd76-278">„Set-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="7fd76-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="7fd76-279">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7fd76-280">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7fd76-281">„New-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="7fd76-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="7fd76-282">„Update-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="7fd76-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="7fd76-283">„New-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="7fd76-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="7fd76-284">„Update-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="7fd76-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-286">Fehler behoben: „PSWorkspace“ implementiert „IOperationalInsightsWorkspace“ nicht [#12135]</span><span class="sxs-lookup"><span data-stu-id="7fd76-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="7fd76-287">„pergb2018“ wurde dem gültigen Satz des Parameters „Sku“ in „Set-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="7fd76-288">Der Alias „FunctionParameters“ für den Parameter „FunctionParameter“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="7fd76-289">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7fd76-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="7fd76-290">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7fd76-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-292">Azure Backup hat Unterstützung für das Abrufen von MAB-Elementen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="7fd76-293">Azure Site Recovery unterstützt Datenträgertyp „StandardSSD_LRS“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-294">Az.Resources</span></span>
* <span data-ttu-id="7fd76-295">„UsageLocation“, „GivenName“, „Surname“, „AccountEnabled“, „MailNickname“, „Mail“ in „PSADUser“ hinzugefügt [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="7fd76-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="7fd76-296">Problem behoben, dass „-Mail“ für „Get-AzADUser“ nicht funktioniert [#11981]</span><span class="sxs-lookup"><span data-stu-id="7fd76-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="7fd76-297">Parameter „-ExcludeChangeType“ zu „Get-AzDeploymentWhatIfResult“ und „Get-AzResourceGroupDeploymentWhatIfResult“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="7fd76-298">Parameter „-WhatIfExcludeChangeType“ zu „New-AzDeployment“ und „New-AzResourceGroupDeployment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="7fd76-299">Cmdlets von „Test-Az\*Deployment“, sodass bessere Fehlermeldungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="7fd76-300">Hilfemeldung für Parameter „-Name“ der Cmdlets „deployment create“ und „What-If“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-301">Az.Sql</span></span>
* <span data-ttu-id="7fd76-302">Unterstützung für Dienstprinzipal für Cmdlet „Set SQL Server Azure Active Directory Admin“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="7fd76-303">Synchronisierungsproblem in Datenklassifizierungs-Cmdlets wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="7fd76-304">Suchen von Benutzern nach E-Mail wird für „Set-AzSqlServerActiveDirectoryAdministrator“ unterstützt [#12192]</span><span class="sxs-lookup"><span data-stu-id="7fd76-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-305">Az.Storage</span></span>
* <span data-ttu-id="7fd76-306">Erstellen eines Speicherkontos mit „RequireInfrastructureEncryption“ wird unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fd76-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="7fd76-307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="7fd76-308">Logik zum Laden von „Azure.Core to Az.Accounts“ verschoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-309">Az.Websites</span></span>
* <span data-ttu-id="7fd76-310">Schutz zum Löschen der erstellten Web-App hinzugefügt, wenn die Wiederherstellung in „Restore-AzDeletedWebApp“ fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7fd76-311">„SourceWebApp.Location“ für „New-AzWebApp“ und „New-AzWebAppSlot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="7fd76-312">Fehler behoben, der das Ändern von Containereinstellungen in „Set-AzWebApp“ und „Set-AzWebAppSlot“ verhindert hat.</span><span class="sxs-lookup"><span data-stu-id="7fd76-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="7fd76-313">Fehler beim Abrufen von „SiteConfig“ behoben, wenn „-Name“ für „Get-AzWebApp“ nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="7fd76-314">Unterstützung zum Erstellen von ASP für Linux-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="7fd76-315">Ausnahmen für den Ressourcengruppen übergreifenden Klonvorgang hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="7fd76-316">4.2.0: Juni 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-317">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-318">Problem behoben, das unter Umständen dazu geführt hat, dass Az Protokolle in Azure Automation- oder PowerShell-Aufträgen übersprungen hat [Nr. 11492]</span><span class="sxs-lookup"><span data-stu-id="7fd76-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fd76-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fd76-320">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-321">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-322">Assemblyversion der Dienstverwaltungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="7fd76-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7fd76-323">Az.Billing</span></span>
* <span data-ttu-id="7fd76-324">Assemblyversion der Nutzungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-326">Unterstützung des PrivateEndpoint- und des PublicNetworkAccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="7fd76-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-327">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-328">Assemblyversion der Data Factory v2-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="7fd76-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-329">Az.DataShare</span></span>
* <span data-ttu-id="7fd76-330">Allgemeine Verfügbarkeit des Moduls „Az.DataShare“</span><span class="sxs-lookup"><span data-stu-id="7fd76-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="7fd76-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="7fd76-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="7fd76-332">Allgemeine Verfügbarkeit des Moduls „Az.DesktopVirtualization“</span><span class="sxs-lookup"><span data-stu-id="7fd76-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-334">SDK auf 0.21.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="7fd76-335">Optionale Parameter hinzugefügt zu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="7fd76-336">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7fd76-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="7fd76-337">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7fd76-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-339">Beispiel 3 für „Start-AzPolicyComplianceScan“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7fd76-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7fd76-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7fd76-341">Assemblyversion der PowerBI-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7fd76-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7fd76-342">Az.PrivateDns</span></span>
* <span data-ttu-id="7fd76-343">Formatierung der ausführlichen Ausgabezeichenfolge für „Remove-AzPrivateDnsRecordSet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-345">Azure Site Recovery-Unterstützung für die Erstellung eines Wiederherstellungsplans für die Replikation zwischen Zonen per XML-Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd76-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="7fd76-346">Assemblyversion der SiteRecovery- und Backup-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-347">Az.Resources</span></span>
* <span data-ttu-id="7fd76-348">Tail-Parameter zu den Cmdlets „Get-AzDeploymentScriptLog“ und „Save-AzDeploymentScriptLog“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="7fd76-349">Die Output-Eigenschaft wurde formatiert und wird nun in der Ausgabe des Cmdlets „Get-AzDeploymentScript“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="7fd76-350">Parameter „-DeploymentScriptInputObject“ in „-DeploymentScriptObject“ umbenannt</span><span class="sxs-lookup"><span data-stu-id="7fd76-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="7fd76-351">Fehlender Datei-/Zielname in Cmdlet-Meldungen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="7fd76-352">Assemblyversion der Resource Manager- und Tags-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-353">Az.Sql</span></span>
* <span data-ttu-id="7fd76-354">„UsePrivateLinkConnection“ zu „New-AzSqlSyncGroup“, „Update-AzSqlSyncGroup“, „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="7fd76-355">„SyncMemberAzureDatabaseResourceId“ zu „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="7fd76-356">Unterstützung für die Gastbenutzersuche zum SQL Server-Cmdlet für den Azure Active Directory-Administrator hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-357">Az.Storage</span></span>
* <span data-ttu-id="7fd76-358">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="7fd76-359">4.1.0 – Mai 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="7fd76-360">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="7fd76-360">Highlights since the last release</span></span>
* <span data-ttu-id="7fd76-361">Unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="7fd76-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="7fd76-362">Allgemeine Verfügbarkeit von Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7fd76-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="7fd76-363">Veröffentlichung von Hauptversionen von Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources und Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-364">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-365">„Add-AzEnvironment“ und „Set-AzEnvironment“ akzeptieren jetzt die Parameter „AzureSynapseAnalyticsEndpointResourceId“ und „AzureSynapseAnalyticsEndpointSuffix“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="7fd76-366">Assemblys zu Azure.Core wurden Az.Accounts hinzugefügt. Unterstützte PowerShell-Plattformen sind u. a. Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="7fd76-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="7fd76-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7fd76-367">Az.Aks</span></span>
* <span data-ttu-id="7fd76-368">API-Version wurde auf 2019-10-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="7fd76-369">Unterstützung für die Erstellung von AKS mit einem Windows-Container</span><span class="sxs-lookup"><span data-stu-id="7fd76-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="7fd76-370">Neu verfügbare Cmdlets: „New-AzAksNodePool“, „Update-AzAksNodePool“, „Remove-AzAksNodePool“, „Get-AzAksNodePool“, „Install-AzAksKubectl“, „Get-AzAksVersion“</span><span class="sxs-lookup"><span data-stu-id="7fd76-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-371">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-372">„New-AzApiManagement“ und „Set-AzApiManagement“: Parameter [-AssignIdentity] wurde in [-SystemAssignedIdentity] umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="7fd76-373">„New-AzApiManagement“ und „Set-AzApiManagement“: Neuer Parameter hinzugefügt: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="7fd76-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="7fd76-374">„Get-AzApiManagementProperty“ wurde in „Get-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7fd76-375">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="7fd76-376">„New-AzApiManagementProperty“ wurde in „New-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7fd76-377">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="7fd76-378">„Set-AzApiManagementProperty“ wurde in „Set-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7fd76-379">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="7fd76-380">„Remove-AzApiManagementProperty“ wurde in „Remove-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7fd76-381">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="7fd76-382">Neues Cmdlet „Get-AzApiManagementAuthorizationServerClientSecret“ hinzugefügt. „Get-AzApiManagementAuthorizationServer“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="7fd76-383">Neues Cmdlet „Get-AzApiManagementNamedValueSecretValue“ hinzugefügt. „Get-AzApiManagementNamedValue“ gibt keinen Geheimniswert zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="7fd76-384">Neues Cmdlet „Get-AzApiManagementOpenIdConnectProviderClientSecret“ hinzugefügt. „Get-AzApiManagementOpenIdConnectProvider“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="7fd76-385">Neues Cmdlet „Get-AzApiManagementSubscriptionKey“ hinzugefügt. „Get-AzApiManagementSubscription“ gibt keine Abonnementschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="7fd76-386">Neues Cmdlet „Get-AzApiManagementTenantAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="7fd76-387">Neues Cmdlet „Get-AzApiManagementTenantGitAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantGitAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7fd76-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7fd76-389">Parameter hinzugefügt: „RetentionInDays“, „PublicNetworkAccessForIngestion“, „PublicNetworkAccessForQuery“ für „New-AzApplicationInsights“</span><span class="sxs-lookup"><span data-stu-id="7fd76-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="7fd76-390">Cmdlet „Update-AzApplicationInsights“ erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="7fd76-391">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-392">Az.Batch</span></span>
* <span data-ttu-id="7fd76-393">Az.Batch für die Verwendung der Microsoft.Azure.Batch-SDK-Version 13.0.0 und der Microsoft.Azure.Management.Batch-SDK-Version 9.0.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="7fd76-394">Die Möglichkeit zum Auswählen der Art des hinzugefügten Zertifikats mithilfe des neuen Parameters „-CertificateKind“ wurde zu „New-AzBatchCertificate“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="7fd76-395">Eigenschaft „ApplicationPackages“ aus „PSApplication“ entfernt, die bislang immer „“ war.</span><span class="sxs-lookup"><span data-stu-id="7fd76-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="7fd76-396">Die spezifischen Pakete in einer Anwendung können jetzt mit „Get-AzBatchApplicationPackage“ abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="7fd76-397">Beispiel: „Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication“</span><span class="sxs-lookup"><span data-stu-id="7fd76-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="7fd76-398">Beim Erstellen eines Pools mit „New-AzBatchPool“ kann die Eigenschaft „VirtualMachineImageId“ von „PSImageReference“ jetzt nur auf ein Bild in einer Shared Image Gallery verweisen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="7fd76-399">Wenn Sie einen Pool mit „New-AzBatchPool“ erstellen, kann der Pool mit der Eigenschaft „PublicIPAddressConfiguration“ von „PSNetworkConfiguration“ ohne eine öffentliche IP-Adresse bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="7fd76-400">Die Eigenschaft „PublicIPs“ von „PSNetworkConfiguration“ wurde ebenfalls in „PSPublicIPAddressConfiguration“ verschoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="7fd76-401">Diese Eigenschaft kann nur angegeben werden, wenn „IPAddressProvisioningType“ den Wert „UserManaged“ hat.</span><span class="sxs-lookup"><span data-stu-id="7fd76-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-402">Az.Compute</span></span>
* <span data-ttu-id="7fd76-403">HostId-Parameter zum Cmdlet „Update-AzVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="7fd76-404">Hilfedokumente für die Cmdlets „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVmss“, „Set-AzVMOperatingSystem“ und „Set-AzVmssOsProfile“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="7fd76-405">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="7fd76-405">Breaking changes</span></span>
    - <span data-ttu-id="7fd76-406">Der FilterExpression-Parameter wurde aus dem Cmdlet „Get-AzVMImage“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="7fd76-407">Der AssignIdentity-Parameter wurde aus den Cmdlets „New-AzVmssConfig“, „New-AzVMConfig“ und „Update-AzVM“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="7fd76-408">AutomaticRepairMaxInstanceRepairsPercent wurde aus den Cmdlets „New-AzVmssConfig“ und „Update-AzVmss“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="7fd76-409">Die Eigenschaften AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus und VirtualMachineScaleSetsColocationStatus wurden aus ProximityPlacementGroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="7fd76-410">Die Eigenschaft MaxInstanceRepairsPercent wurde aus AutomaticRepairsPolicy entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="7fd76-411">Die Typen von AvailabilitySets, VirtualMachines und VirtualMachineScaleSets wurden von IList<SubResource> in IList<SubResourceWithColocationStatus> geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="7fd76-412">Die Beschreibung für das Cmdlet „Get-AzVM“ wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-413">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-414">CRUD von Datenfluss-Laufzeiteigenschaften in Managed IR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-415">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-416">Neue Cmdlets zum Erstellen, Aktualisieren, Abrufen und Löschen von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="7fd76-417">Hilfs-Cmdlets für die Erstellung von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="7fd76-418">Regelmodulverweis auf Front Door-Routingregelobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="7fd76-419">Private Link-Parameter zum Front Door-Back-End-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="7fd76-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7fd76-420">Az.Functions</span></span>
* <span data-ttu-id="7fd76-421">Allgemeine Verfügbarkeit des Moduls „Az.Functions“</span><span class="sxs-lookup"><span data-stu-id="7fd76-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-422">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-423">Datenträgerverschlüsselung mit kundenseitig verwalteten Schlüsseln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7fd76-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7fd76-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="7fd76-425">Zugriffsrichtlinien verwenden nicht mehr den aktuellen Prinzipal als Standard.</span><span class="sxs-lookup"><span data-stu-id="7fd76-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-426">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-427">Cmdlet zum Aufrufen einer Abfrage in einem IoT-Hub zum Abrufen von Informationen mithilfe einer SQL-ähnlichen Sprache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="7fd76-428">Problem behoben, dass „Add-AzIotHubDevice“ kein Edge-aktiviertes Gerät ohne untergeordnete Geräte erstellen konnte. [#11597]</span><span class="sxs-lookup"><span data-stu-id="7fd76-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="7fd76-429">Cmdlet zum Generieren eines SAS-Tokens für IoT-Hub, -Gerät oder -Modul hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="7fd76-430">Cmdlet zum Aufrufen der Konfigurationsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="7fd76-431">Verwalten der automatischen skalierbaren Bereitstellung von IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="7fd76-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="7fd76-432">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-432">New cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-433">„Add-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="7fd76-434">„Get-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="7fd76-435">„Remove-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="7fd76-436">„Set-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="7fd76-437">Cmdlet zum Hinzufügen einer IoT Edge-Bereitstellungsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="7fd76-438">Cmdlet zum Anwenden des Konfigurationsinhalts auf das angegebene Edge-Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-439">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-440">Zwei Aliase entfernt: „New-AzKeyVaultCertificateAdministratorDetails“ und „New-AzKeyVaultCertificateOrganizationDetails“</span><span class="sxs-lookup"><span data-stu-id="7fd76-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="7fd76-441">Vorläufiges Löschen ist beim Erstellen eines Schlüsseltresors standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="7fd76-442">Netzwerkregeln können so festgelegt werden, dass der Zugriff von bestimmten Netzwerkstandorten beim Erstellen eines Schlüsseltresors gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="7fd76-443">Unterstützung für BYOK (Bring Your Own Key) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="7fd76-444">„Add-AzKeyVaultKey“ unterstützt die Erstellung eines Schlüsselaustauschschlüssels.</span><span class="sxs-lookup"><span data-stu-id="7fd76-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="7fd76-445">„Get-AzKeyVaultKey“ unterstützt das Herunterladen eines öffentlichen Schlüssels im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="7fd76-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="7fd76-446">Abschnitt „KeyOps“ der Hilfedokumentation zu „Add-AzKeyVaultKey“ wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-447">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-448">Fehler bei „Set-AzDiagnosticSettings“ behoben. Aufbewahrungsrichtlinie gilt nicht für alle Kategorien. [#11589]</span><span class="sxs-lookup"><span data-stu-id="7fd76-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="7fd76-449">WebTest-Verfügbarkeitskriterien für die Metrikwarnung V2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="7fd76-450">„New-AzMetricAlertRuleV2Criteria“: Option zum Erstellen der Webtest-Verfügbarkeitskriterien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="7fd76-451">„Add-AzMetricAlertRuleV2“: Neue Webtest-Verfügbarkeitskriterien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="7fd76-452">Redundante Definition für „RetentionPolicy“ in PSLogProfile entfernt. [#7608]</span><span class="sxs-lookup"><span data-stu-id="7fd76-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="7fd76-453">Redundante in PSEventData definierte Eigenschaften entfernt. [#11353]</span><span class="sxs-lookup"><span data-stu-id="7fd76-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="7fd76-454">„Get-AzLog“ in „Get-AzActivityLog“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-455">Az.Network</span></span>
* <span data-ttu-id="7fd76-456">Breaking Change-Attribut hinzugefügt als Benachrichtigung, dass sich das Standardverhalten der Zone ändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="7fd76-457">„New-AzPublicIpAddress“</span><span class="sxs-lookup"><span data-stu-id="7fd76-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="7fd76-458">„New-AzPublicIpPrefix“</span><span class="sxs-lookup"><span data-stu-id="7fd76-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="7fd76-459">„New-AzLoadBalancerFrontendIpConfig“</span><span class="sxs-lookup"><span data-stu-id="7fd76-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="7fd76-460">Unterstützung für die neue Ressource der obersten Ebene SecurityPartnerProvider hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="7fd76-461">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-461">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-462">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7fd76-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="7fd76-463">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7fd76-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="7fd76-464">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7fd76-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="7fd76-465">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7fd76-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="7fd76-466">„RequiredZoneNames“ für „PSPrivateLinkResource“ und „GroupId“ für „PSPrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="7fd76-467">Falscher Typ des Parameters SuccessThresholdRoundTripTimeMs für New-AzNetworkWatcherConnectionMonitorTestConfigurationObject korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="7fd76-468">VirtualWan-Cmdlets aktualisiert, sodass der Standardwert des Arguments AllowVnetToVnetTraffic auf True festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="7fd76-469">„New-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="7fd76-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="7fd76-470">„Update-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="7fd76-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="7fd76-471">Neue Cmdlets zur Unterstützung der DNS-Zonengruppe für den privaten Endpunkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="7fd76-472">„New-AzPrivateDnsZoneConfig“</span><span class="sxs-lookup"><span data-stu-id="7fd76-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="7fd76-473">„Get-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="7fd76-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="7fd76-474">„New-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="7fd76-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="7fd76-475">„Set-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="7fd76-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="7fd76-476">„Remove-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="7fd76-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="7fd76-477">Parameter „DNSEnableProxy“, „DNSRequireProxyForNetworkRules“ und „DNSServers“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="7fd76-478">Parameter „EnableDnsProxy“, „DnsProxyNotRequiredForNetworkRule“ und „DnsServer“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="7fd76-479">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7fd76-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="7fd76-480">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7fd76-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-482">Legacycode zum Anwenden des neuen generierten SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="7fd76-483">Cmdlets aufgrund von veralteten APIs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7fd76-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="7fd76-484">„Get-AzOperationalInsightsSavedSearchResult“ (alias „Get-AzOperationalInsightsSavedSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="7fd76-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="7fd76-485">„Get-AzOperationalInsightsSearchResult“ (alias „Get-AzOperationalInsightsSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="7fd76-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="7fd76-486">„Get-AzOperationalInsightsLinkTarget“ (alias „Get-AzOperationalInsightsLinkTargets“)</span><span class="sxs-lookup"><span data-stu-id="7fd76-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="7fd76-487">Parameter für „Set-AzOperationalInsightsWorkspace“ und „New-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="7fd76-488">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="7fd76-489">Cmdlets für Cluster und verknüpften Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-491">Azure Site Recovery: Unterstützung für den Schutz von virtuellen Computern der Näherungsplatzierungsgruppe für den Azure-zu-Azure-Anbieter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="7fd76-492">Azure Site Recovery: Unterstützung für die Replikation zwischen Zonen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="7fd76-493">Azure Backup: Unterstützung für die langfristige Aufbewahrung von Azure FileShare-Wiederherstellungspunkten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="7fd76-494">Azure Backup: Eigenschaften für den Ausschluss von Datenträgern zur Ausgabe des Cmdlet „Get-AzRecoveryServicesBackupItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="7fd76-495">Privater Endpunkt für Tresoranmeldeinformationen für den Site Recovery-Dienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-496">Az.Resources</span></span>
* <span data-ttu-id="7fd76-497">Warnmeldung zur verzögerten Ansicht beim Erstellen einer neuen Rollendefinition hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="7fd76-498">Richtlinien-Cmdlets geändert, sodass sie stark typisierte Objekte ausgeben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="7fd76-499">Parameter „-TenantLevel“ zum Cmdlet „Get-AzResourceLock“ hinzugefügt. [#11335]</span><span class="sxs-lookup"><span data-stu-id="7fd76-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="7fd76-500">„Remove-AzResourceGroup -Id ResourceId“ korrigiert. [#9882]</span><span class="sxs-lookup"><span data-stu-id="7fd76-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="7fd76-501">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Ressourcengruppenbereich hinzugefügt: „Get-AzDeploymentResourceGroupWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="7fd76-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="7fd76-502">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Abonnementbereich hinzugefügt: „Get-AzDeploymentWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="7fd76-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="7fd76-503">Alias: „Get-AzSubscriptionDeploymentWhatIf“</span><span class="sxs-lookup"><span data-stu-id="7fd76-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="7fd76-504">Parameter „-WhatIf“ und „-Confirm“ für „New-AzDeployment“ und „New-AzResourceGroupDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="7fd76-505">Meldung zur Einstellung der Unterstützung für „ApiVersion“ in Bereitstellungs-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="7fd76-506">Funktion zum Anzeigen verbesserter Fehlermeldungen für Bereitstellungsfehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="7fd76-507">Protokollierung von correlationId bei Bereitstellungsfehlern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="7fd76-508">Eigenschaft „error“ zur Bereitstellungsskriptausgabe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="7fd76-509">NuGet-Microsoft.Azure.Management.ResourceManager auf „3.7.1-preview“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="7fd76-510">Bestimmte Testfälle entfernt, da die Error-Eigenschaft in DeploymentValidateResult von NuGet 3.7.1-preview in schreibgeschützt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd76-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="7fd76-511">GenericResourceExpanded aus dem SDK ResourceManager 3.7.1-preview importiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="7fd76-512">Tagunterstützung für alle Get-Cmdlets für die Bereitstellung hinzugefügt sowie</span><span class="sxs-lookup"><span data-stu-id="7fd76-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="7fd76-513">„New-AzDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="7fd76-514">„New-AzManagementGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="7fd76-515">„New-AzResourceGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7fd76-516">„New-AzTenantDeployment“</span><span class="sxs-lookup"><span data-stu-id="7fd76-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-518">Fehler beim Hinzufügen eines Zertifikats mithilfe von „--SecretIdentifier“ behoben, der den falschen Zertifikatfingerabdruck erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="7fd76-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-519">Az.Sql</span></span>
* <span data-ttu-id="7fd76-520">Leistungsoptimierung von:</span><span class="sxs-lookup"><span data-stu-id="7fd76-520">Enhance performance of:</span></span>
    - <span data-ttu-id="7fd76-521">„Set-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="7fd76-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7fd76-522">„Set-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="7fd76-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7fd76-523">„Remove-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="7fd76-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7fd76-524">„Remove-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="7fd76-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7fd76-525">„Enable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="7fd76-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="7fd76-526">„Enable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="7fd76-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="7fd76-527">„Disable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="7fd76-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="7fd76-528">„Disable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="7fd76-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="7fd76-529">Clientseitige Validierung des Parameters „RetentionDays“ aus dem Cmdlet „Set-AzSqlDatabaseBackupShortTermRetentionPolicy“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="7fd76-530">Fehler beim Überwachen eines Speicherkontos in Vnet und Erstellen einer Rolle für den Mitwirkenden an Speicherblobdaten behoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-531">Az.Storage</span></span>
* <span data-ttu-id="7fd76-532">„-AsJob“ hinzugefügt, um das Konto für das Cmdlet „Get-AzStorageAccount“ abzurufen/aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="7fd76-533">KeyVersion als optional festgelegt, wenn das Speicherkonto mit KeyvaultEncryption aktualisiert wird, um die automatische Schlüsselrotation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="7fd76-534">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7fd76-535">Fehler beim Entfernen des Azure-Dateiverzeichnisses mit der Pipeline behoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="7fd76-536">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="7fd76-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="7fd76-537">Behoben [#9880]: Definition des DefaultAction-Werts für NetWorkRule in Übereinstimmung mit Swagger geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="7fd76-538">„Update-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="7fd76-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="7fd76-539">„Get-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="7fd76-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="7fd76-540">Behoben [#11624]: Doppelte Regeln werden beim Hinzufügen von NetworkRules übersprungen, um Serverfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="7fd76-541">„Add-AzStorageAccountNetworkRule“</span><span class="sxs-lookup"><span data-stu-id="7fd76-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="7fd76-542">Microsoft.Azure.Cosmos.Table SDK auf 1.0.7 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="7fd76-543">Warnmeldung hinzugefügt, mit der der Benutzer darauf hingewiesen wird, eine erneute Auflistung mit ContinuationToken auszuführen, wenn nur ein Teil der Elemente in der Liste der DataLake Gen2-Elemente zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="7fd76-544">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="7fd76-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="7fd76-545">Unterstützung für das Erstellen oder Aktualisieren eines Speicherkontos mit Active Directory Domain Service-Authentifizierung für Azure Files.</span><span class="sxs-lookup"><span data-stu-id="7fd76-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="7fd76-546">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="7fd76-547">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7fd76-548">Unterstützung für das Hinzufügen und Auflisten von Kerberos-Schlüsseln des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="7fd76-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="7fd76-549">„New-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="7fd76-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="7fd76-550">„Get-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="7fd76-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7fd76-551">Unterstützung für Failover für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="7fd76-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="7fd76-552">„Invoke-AzStorageAccountFailover“</span><span class="sxs-lookup"><span data-stu-id="7fd76-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="7fd76-553">Hilfe zu „Get-AzStorageBlobCopyState“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="7fd76-554">Hilfe zu „Get-AzStorageFileCopyState“ und „Start-AzStorageBlobCopy“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="7fd76-555">Speicherclientbibliothek v12 in Cmdlets Queue und File integriert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="7fd76-556">Ausgabetyp von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7fd76-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="7fd76-557">„Get-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="7fd76-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="7fd76-558">„Remove-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="7fd76-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="7fd76-559">„Get-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="7fd76-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="7fd76-560">„Set-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="7fd76-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="7fd76-561">„Start-AzStorageFileCopy“</span><span class="sxs-lookup"><span data-stu-id="7fd76-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="7fd76-562">Ausgabetyp von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7fd76-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="7fd76-563">„New-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="7fd76-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="7fd76-564">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="7fd76-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="7fd76-565">Ausgabetyp von CloudFileShare in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7fd76-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="7fd76-566">„Get-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="7fd76-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="7fd76-567">„New-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="7fd76-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="7fd76-568">„Remove-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="7fd76-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="7fd76-569">Ausgabetyp von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7fd76-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="7fd76-570">„Set-AzStorageShareQuota“</span><span class="sxs-lookup"><span data-stu-id="7fd76-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7fd76-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7fd76-571">Az.TrafficManager</span></span>
* <span data-ttu-id="7fd76-572">Falscher Profilname in der ausführlichen Ausgabe von „DisableAzureTrafficManagerEndpoint“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-573">Az.Websites</span></span>
* <span data-ttu-id="7fd76-574">Tippfehler in der Hilfe zu „Update-AzWebAppAccessRestrictionConfig“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="7fd76-575">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="7fd76-576">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="7fd76-576">Highlights since the last release</span></span>
* <span data-ttu-id="7fd76-577">Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="7fd76-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-578">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-579">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="7fd76-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-580">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-581">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="7fd76-582">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-583">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-584">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-586">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="7fd76-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-587">Az.Compute</span></span>
* <span data-ttu-id="7fd76-588">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="7fd76-589">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="7fd76-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-590">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-591">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-592">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7fd76-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="7fd76-593">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7fd76-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="7fd76-594">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="7fd76-595">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-596">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="7fd76-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="7fd76-597">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="7fd76-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="7fd76-598">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="7fd76-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="7fd76-599">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-599">New cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-600">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="7fd76-601">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="7fd76-602">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="7fd76-603">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="7fd76-604">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-605">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-606">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fd76-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="7fd76-607">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="7fd76-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="7fd76-608">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="7fd76-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="7fd76-609">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="7fd76-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="7fd76-610">Az.Maintenance</span></span>
* <span data-ttu-id="7fd76-611">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-612">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-613">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="7fd76-614">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7fd76-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7fd76-615">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7fd76-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7fd76-616">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7fd76-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7fd76-617">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7fd76-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7fd76-618">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="7fd76-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="7fd76-619">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="7fd76-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="7fd76-620">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="7fd76-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-621">Az.Network</span></span>
* <span data-ttu-id="7fd76-622">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="7fd76-623">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="7fd76-624">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="7fd76-625">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="7fd76-626">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="7fd76-627">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="7fd76-628">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="7fd76-629">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7fd76-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="7fd76-630">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="7fd76-631">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="7fd76-632">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="7fd76-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="7fd76-633">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="7fd76-634">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="7fd76-635">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="7fd76-636">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="7fd76-637">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-639">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="7fd76-640">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-642">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7fd76-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-643">Az.Sql</span></span>
* <span data-ttu-id="7fd76-644">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="7fd76-645">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="7fd76-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-646">Az.Storage</span></span>
* <span data-ttu-id="7fd76-647">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="7fd76-648">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="7fd76-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="7fd76-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="7fd76-650">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7fd76-651">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="7fd76-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="7fd76-652">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7fd76-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7fd76-653">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7fd76-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7fd76-654">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="7fd76-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="7fd76-655">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7fd76-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7fd76-656">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="7fd76-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="7fd76-657">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7fd76-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7fd76-658">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="7fd76-659">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7fd76-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="7fd76-660">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="7fd76-661">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-661">General</span></span>
* <span data-ttu-id="7fd76-662">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fd76-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="7fd76-663">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="7fd76-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="7fd76-664">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="7fd76-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="7fd76-665">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="7fd76-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="7fd76-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7fd76-666">Az.Billing</span></span>
  - <span data-ttu-id="7fd76-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-667">Az.Compute</span></span>
  - <span data-ttu-id="7fd76-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7fd76-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="7fd76-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-669">Az.EventHub</span></span>
  - <span data-ttu-id="7fd76-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-670">Az.IotHub</span></span>
  - <span data-ttu-id="7fd76-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-671">Az.KeyVault</span></span>
  - <span data-ttu-id="7fd76-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-672">Az.Monitor</span></span>
  - <span data-ttu-id="7fd76-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-673">Az.Network</span></span>
  - <span data-ttu-id="7fd76-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-674">Az.Resources</span></span>
  - <span data-ttu-id="7fd76-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-675">Az.Storage</span></span>
  - <span data-ttu-id="7fd76-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-676">Az.Websites</span></span>
* <span data-ttu-id="7fd76-677">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7fd76-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="7fd76-678">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="7fd76-679">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="7fd76-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="7fd76-680">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-681">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-682">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="7fd76-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-683">Az.Compute</span></span>
* <span data-ttu-id="7fd76-684">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="7fd76-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="7fd76-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="7fd76-686">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="7fd76-687">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="7fd76-688">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="7fd76-688">[#11354]</span></span>
* <span data-ttu-id="7fd76-689">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="7fd76-690">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7fd76-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7fd76-691">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7fd76-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7fd76-692">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7fd76-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7fd76-693">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7fd76-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="7fd76-694">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="7fd76-695">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="7fd76-696">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="7fd76-697">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="7fd76-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-698">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-699">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="7fd76-700">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-702">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="7fd76-703">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-704">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-705">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fd76-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-706">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-707">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="7fd76-708">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-709">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="7fd76-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="7fd76-710">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="7fd76-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-711">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-712">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-713">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-714">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-715">Az.Network</span></span>
* <span data-ttu-id="7fd76-716">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="7fd76-717">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7fd76-718">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7fd76-719">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="7fd76-720">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="7fd76-721">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-723">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="7fd76-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-725">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="7fd76-726">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="7fd76-727">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="7fd76-728">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="7fd76-729">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="7fd76-730">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-731">Az.Resources</span></span>
* <span data-ttu-id="7fd76-732">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="7fd76-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="7fd76-733">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="7fd76-734">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="7fd76-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="7fd76-735">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-735">Added example.</span></span>
* <span data-ttu-id="7fd76-736">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="7fd76-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="7fd76-737">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-738">Az.Sql</span></span>
* <span data-ttu-id="7fd76-739">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="7fd76-740">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="7fd76-741">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="7fd76-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="7fd76-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="7fd76-742">Az.Support</span></span>
* <span data-ttu-id="7fd76-743">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="7fd76-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-744">Az.Websites</span></span>
* <span data-ttu-id="7fd76-745">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="7fd76-746">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7fd76-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7fd76-747">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7fd76-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7fd76-748">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7fd76-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7fd76-749">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7fd76-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="7fd76-750">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-751">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-752">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="7fd76-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="7fd76-753">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="7fd76-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="7fd76-754">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-755">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-756">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="7fd76-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="7fd76-757">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="7fd76-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="7fd76-758">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="7fd76-759">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="7fd76-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-761">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-762">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-763">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7fd76-764">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-765">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7fd76-766">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7fd76-767">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7fd76-768">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="7fd76-769">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="7fd76-770">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-771">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7fd76-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="7fd76-772">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7fd76-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="7fd76-773">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7fd76-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="7fd76-774">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7fd76-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="7fd76-775">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7fd76-776">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7fd76-777">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="7fd76-778">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-779">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="7fd76-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="7fd76-780">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="7fd76-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="7fd76-781">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-782">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-783">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="7fd76-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-784">Az.Network</span></span>
* <span data-ttu-id="7fd76-785">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="7fd76-786">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="7fd76-787">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="7fd76-788">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-789">Az.Resources</span></span>
* <span data-ttu-id="7fd76-790">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="7fd76-791">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="7fd76-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="7fd76-792">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="7fd76-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="7fd76-793">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="7fd76-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="7fd76-794">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="7fd76-795">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="7fd76-796">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="7fd76-797">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="7fd76-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd76-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7fd76-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd76-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7fd76-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd76-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="7fd76-801">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="7fd76-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd76-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="7fd76-803">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="7fd76-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-804">Az.Sql</span></span>
* <span data-ttu-id="7fd76-805">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="7fd76-806">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="7fd76-807">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="7fd76-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="7fd76-808">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="7fd76-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="7fd76-809">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="7fd76-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="7fd76-810">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="7fd76-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="7fd76-811">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="7fd76-812">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="7fd76-813">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="7fd76-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-814">Az.Storage</span></span>
* <span data-ttu-id="7fd76-815">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="7fd76-816">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="7fd76-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="7fd76-817">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="7fd76-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="7fd76-818">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="7fd76-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="7fd76-819">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="7fd76-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-820">Az.Websites</span></span>
* <span data-ttu-id="7fd76-821">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="7fd76-822">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="7fd76-823">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="7fd76-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="7fd76-824">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="7fd76-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="7fd76-825">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="7fd76-826">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fd76-827">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7fd76-827">Highlights since the last major release</span></span>
* <span data-ttu-id="7fd76-828">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="7fd76-829">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="7fd76-830">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-831">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-832">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-833">Az.Automation</span></span>
* <span data-ttu-id="7fd76-834">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-836">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="7fd76-837">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="7fd76-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-838">Az.Compute</span></span>
* <span data-ttu-id="7fd76-839">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="7fd76-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-840">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-841">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="7fd76-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-842">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-843">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7fd76-844">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-845">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7fd76-846">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7fd76-847">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7fd76-848">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7fd76-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-849">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-850">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-851">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-852">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="7fd76-853">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="7fd76-854">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-855">Az.Network</span></span>
* <span data-ttu-id="7fd76-856">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="7fd76-857">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7fd76-858">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7fd76-859">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="7fd76-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="7fd76-860">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-860">No new cmdlets are added.</span></span> <span data-ttu-id="7fd76-861">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-863">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-864">Az.Resources</span></span>
* <span data-ttu-id="7fd76-865">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="7fd76-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="7fd76-866">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7fd76-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="7fd76-867">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7fd76-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="7fd76-868">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="7fd76-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="7fd76-869">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="7fd76-870">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="7fd76-871">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="7fd76-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="7fd76-872">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-873">Az.Sql</span></span>
* <span data-ttu-id="7fd76-874">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="7fd76-875">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="7fd76-876">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7fd76-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7fd76-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7fd76-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7fd76-878">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7fd76-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7fd76-879">Az.StorageSync</span></span>
* <span data-ttu-id="7fd76-880">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="7fd76-881">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fd76-882">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7fd76-882">Highlights since the last major release</span></span>
* <span data-ttu-id="7fd76-883">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="7fd76-884">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-885">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-886">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="7fd76-887">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="7fd76-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-888">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-889">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="7fd76-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="7fd76-890">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="7fd76-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="7fd76-891">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="7fd76-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="7fd76-892">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-893">Az.Compute</span></span>
* <span data-ttu-id="7fd76-894">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="7fd76-895">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="7fd76-896">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="7fd76-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="7fd76-898">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-899">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-900">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7fd76-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7fd76-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="7fd76-902">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="7fd76-903">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-904">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-905">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-906">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-907">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="7fd76-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-908">Az.Network</span></span>
* <span data-ttu-id="7fd76-909">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="7fd76-910">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="7fd76-911">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7fd76-912">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="7fd76-913">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="7fd76-914">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="7fd76-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="7fd76-915">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="7fd76-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="7fd76-916">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="7fd76-917">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-917">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="7fd76-919">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="7fd76-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="7fd76-921">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-923">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7fd76-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="7fd76-924">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="7fd76-925">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="7fd76-926">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-928">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="7fd76-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="7fd76-929">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-930">Az.Resources</span></span>
* <span data-ttu-id="7fd76-931">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="7fd76-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="7fd76-932">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-933">Az.Sql</span></span>
<span data-ttu-id="7fd76-934">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="7fd76-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-935">Az.Storage</span></span>
* <span data-ttu-id="7fd76-936">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="7fd76-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="7fd76-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="7fd76-938">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="7fd76-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="7fd76-939">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-940">Az.Websites</span></span>
* <span data-ttu-id="7fd76-941">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="7fd76-942">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd76-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="7fd76-943">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="7fd76-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-944">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-945">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="7fd76-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-946">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-947">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="7fd76-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-948">Az.Compute</span></span>
* <span data-ttu-id="7fd76-949">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7fd76-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="7fd76-951">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7fd76-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7fd76-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7fd76-953">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7fd76-954">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="7fd76-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="7fd76-955">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7fd76-956">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="7fd76-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="7fd76-957">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7fd76-958">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="7fd76-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="7fd76-959">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7fd76-960">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="7fd76-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="7fd76-961">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7fd76-962">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="7fd76-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="7fd76-963">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7fd76-964">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="7fd76-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="7fd76-965">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7fd76-966">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="7fd76-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="7fd76-967">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="7fd76-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="7fd76-968">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="7fd76-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="7fd76-969">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="7fd76-970">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="7fd76-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-971">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-972">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="7fd76-973">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="7fd76-974">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="7fd76-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7fd76-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="7fd76-976">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-977">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-978">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-979">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-980">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7fd76-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7fd76-981">Az.MachineLearning</span></span>
* <span data-ttu-id="7fd76-982">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="7fd76-983">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7fd76-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="7fd76-984">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="7fd76-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="7fd76-985">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7fd76-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="7fd76-986">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7fd76-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="7fd76-987">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7fd76-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="7fd76-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="7fd76-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="7fd76-989">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="7fd76-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-990">Az.Network</span></span>
* <span data-ttu-id="7fd76-991">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="7fd76-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-993">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="7fd76-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="7fd76-994">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="7fd76-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7fd76-995">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="7fd76-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7fd76-996">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="7fd76-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-997">Az.Resources</span></span>
* <span data-ttu-id="7fd76-998">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-999">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1000">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="7fd76-1001">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7fd76-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7fd76-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7fd76-1003">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1004">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1005">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="7fd76-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="7fd76-1006">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="7fd76-1007">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="7fd76-1008">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="7fd76-1009">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="7fd76-1010">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-1010">General</span></span>
* <span data-ttu-id="7fd76-1011">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1012">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1013">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="7fd76-1014">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-1015">Az.Batch</span></span>
* <span data-ttu-id="7fd76-1016">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1017">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1018">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-1020">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="7fd76-1021">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7fd76-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7fd76-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="7fd76-1023">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="7fd76-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-1024">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-1025">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="7fd76-1026">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="7fd76-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="7fd76-1027">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1028">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-1029">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="7fd76-1030">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="7fd76-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="7fd76-1031">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1032">Az.Network</span></span>
* <span data-ttu-id="7fd76-1033">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="7fd76-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1034">Az.Resources</span></span>
* <span data-ttu-id="7fd76-1035">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="7fd76-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="7fd76-1036">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1037">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1038">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1039">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1040">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7fd76-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="7fd76-1041">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7fd76-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="7fd76-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7fd76-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="7fd76-1043">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="7fd76-1044">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="7fd76-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="7fd76-1045">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="7fd76-1046">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="7fd76-1047">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="7fd76-1048">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="7fd76-1049">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="7fd76-1050">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="7fd76-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="7fd76-1051">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="7fd76-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="7fd76-1052">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7fd76-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="7fd76-1053">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fd76-1054">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7fd76-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="7fd76-1055">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7fd76-1056">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1057">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1058">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="7fd76-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="7fd76-1059">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7fd76-1060">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7fd76-1061">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7fd76-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7fd76-1062">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7fd76-1063">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7fd76-1064">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7fd76-1065">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7fd76-1066">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7fd76-1067">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7fd76-1068">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7fd76-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7fd76-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7fd76-1070">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7fd76-1071">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1071">Get the Order</span></span>
* <span data-ttu-id="7fd76-1072">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7fd76-1073">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1073">Create new Order</span></span>
* <span data-ttu-id="7fd76-1074">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7fd76-1075">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1075">Remove the Order</span></span>
* <span data-ttu-id="7fd76-1076">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="7fd76-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7fd76-1077">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="7fd76-1077">Now creates Local Share</span></span>
* <span data-ttu-id="7fd76-1078">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7fd76-1079">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7fd76-1080">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7fd76-1081">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="7fd76-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7fd76-1082">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7fd76-1083">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="7fd76-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="7fd76-1084">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7fd76-1085">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1085">Create new Triggers</span></span>
* <span data-ttu-id="7fd76-1086">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7fd76-1087">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1088">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1089">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7fd76-1090">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-1092">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1093">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-1094">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-1096">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7fd76-1097">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7fd76-1098">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7fd76-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7fd76-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1100">Az.Network</span></span>
* <span data-ttu-id="7fd76-1101">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7fd76-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7fd76-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="7fd76-1103">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1105">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7fd76-1106">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7fd76-1107">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7fd76-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7fd76-1108">Az.RedisCache</span></span>
* <span data-ttu-id="7fd76-1109">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7fd76-1110">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7fd76-1111">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1112">Az.Resources</span></span>
- <span data-ttu-id="7fd76-1113">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7fd76-1114">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="7fd76-1115">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7fd76-1116">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7fd76-1117">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1118">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1119">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7fd76-1120">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7fd76-1121">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7fd76-1122">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-1122">General</span></span>
* <span data-ttu-id="7fd76-1123">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1124">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1125">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7fd76-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1126">Az.Advisor</span></span>
* <span data-ttu-id="7fd76-1127">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-1128">Az.Batch</span></span>
* <span data-ttu-id="7fd76-1129">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7fd76-1130">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7fd76-1131">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7fd76-1132">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7fd76-1133">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7fd76-1134">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7fd76-1135">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7fd76-1136">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7fd76-1137">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7fd76-1138">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7fd76-1139">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7fd76-1140">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7fd76-1141">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7fd76-1142">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7fd76-1143">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7fd76-1144">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7fd76-1145">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7fd76-1146">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7fd76-1147">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7fd76-1148">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="7fd76-1149">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7fd76-1150">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7fd76-1151">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7fd76-1152">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="7fd76-1153">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7fd76-1154">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="7fd76-1155">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7fd76-1156">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7fd76-1157">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7fd76-1158">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7fd76-1159">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7fd76-1160">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7fd76-1161">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7fd76-1162">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7fd76-1163">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="7fd76-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7fd76-1164">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="7fd76-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-1165">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-1166">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7fd76-1167">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1168">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1169">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7fd76-1170">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7fd76-1171">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7fd76-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7fd76-1172">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7fd76-1173">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7fd76-1174">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7fd76-1175">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7fd76-1176">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1176">Breaking changes</span></span>
    - <span data-ttu-id="7fd76-1177">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7fd76-1178">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1179">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1180">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-1182">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7fd76-1183">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="7fd76-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7fd76-1184">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7fd76-1185">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="7fd76-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7fd76-1186">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="7fd76-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7fd76-1187">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="7fd76-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-1189">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-1190">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-1191">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7fd76-1192">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7fd76-1193">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7fd76-1194">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7fd76-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7fd76-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7fd76-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7fd76-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7fd76-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7fd76-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7fd76-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7fd76-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7fd76-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7fd76-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7fd76-1200">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="7fd76-1201">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7fd76-1202">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7fd76-1203">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7fd76-1204">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7fd76-1205">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7fd76-1206">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7fd76-1207">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7fd76-1208">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7fd76-1209">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7fd76-1210">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7fd76-1211">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="7fd76-1212">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1213">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-1214">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1214">Breaking changes:</span></span>
    - <span data-ttu-id="7fd76-1215">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7fd76-1216">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7fd76-1217">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7fd76-1218">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7fd76-1219">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7fd76-1220">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7fd76-1221">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7fd76-1222">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7fd76-1223">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7fd76-1224">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7fd76-1225">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7fd76-1226">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1228">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-1229">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7fd76-1230">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7fd76-1231">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-1232">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-1233">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-1234">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-1235">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-1236">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1237">Az.Resources</span></span>
* <span data-ttu-id="7fd76-1238">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1239">Az.Network</span></span>
* <span data-ttu-id="7fd76-1240">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7fd76-1241">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="7fd76-1242">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1243">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1244">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1245">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7fd76-1247">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7fd76-1248">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1248">New cmdlet:</span></span>
        - <span data-ttu-id="7fd76-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7fd76-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7fd76-1250">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7fd76-1251">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7fd76-1252">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7fd76-1253">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7fd76-1254">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7fd76-1255">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7fd76-1256">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7fd76-1257">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7fd76-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7fd76-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7fd76-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7fd76-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7fd76-1263">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7fd76-1264">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7fd76-1265">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7fd76-1266">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7fd76-1267">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7fd76-1268">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7fd76-1269">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7fd76-1270">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7fd76-1272">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7fd76-1273">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7fd76-1274">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7fd76-1275">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7fd76-1276">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7fd76-1277">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7fd76-1278">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7fd76-1279">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7fd76-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7fd76-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7fd76-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7fd76-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7fd76-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7fd76-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7fd76-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7fd76-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7fd76-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7fd76-1286">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7fd76-1287">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7fd76-1288">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7fd76-1289">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7fd76-1290">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7fd76-1291">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7fd76-1292">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7fd76-1293">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7fd76-1294">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7fd76-1295">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7fd76-1296">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7fd76-1297">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7fd76-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="7fd76-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7fd76-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7fd76-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7fd76-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7fd76-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7fd76-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-1303">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1304">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1305">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7fd76-1306">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7fd76-1307">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7fd76-1308">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7fd76-1309">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7fd76-1310">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7fd76-1311">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7fd76-1312">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="7fd76-1313">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1314">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1315">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7fd76-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7fd76-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7fd76-1318">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7fd76-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7fd76-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7fd76-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7fd76-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="7fd76-1321">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7fd76-1322">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-1322">General</span></span>
* <span data-ttu-id="7fd76-1323">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7fd76-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1324">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1325">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-1327">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7fd76-1328">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="7fd76-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-1329">Az.Automation</span></span>
* <span data-ttu-id="7fd76-1330">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-1331">Az.Batch</span></span>
* <span data-ttu-id="7fd76-1332">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1333">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1334">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7fd76-1335">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7fd76-1336">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="7fd76-1337">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1338">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1339">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="7fd76-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7fd76-1340">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7fd76-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7fd76-1341">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-1343">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="7fd76-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7fd76-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7fd76-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="7fd76-1345">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7fd76-1346">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7fd76-1347">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7fd76-1348">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1349">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-1350">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="7fd76-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7fd76-1351">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1352">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-1353">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="7fd76-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7fd76-1354">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7fd76-1355">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7fd76-1356">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1357">Az.Network</span></span>
* <span data-ttu-id="7fd76-1358">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="7fd76-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7fd76-1359">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7fd76-1360">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-1361">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7fd76-1362">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7fd76-1363">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7fd76-1364">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="7fd76-1365">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7fd76-1366">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7fd76-1367">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7fd76-1368">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7fd76-1369">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7fd76-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7fd76-1370">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7fd76-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7fd76-1371">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7fd76-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7fd76-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7fd76-1372">Az.RedisCache</span></span>
* <span data-ttu-id="7fd76-1373">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1374">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1375">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1376">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1377">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7fd76-1378">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="7fd76-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7fd76-1379">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7fd76-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7fd76-1380">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="7fd76-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7fd76-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7fd76-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7fd76-1382">Az.StorageSync</span></span>
* <span data-ttu-id="7fd76-1383">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-1384">Az.Websites</span></span>
* <span data-ttu-id="7fd76-1385">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7fd76-1386">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-1388">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7fd76-1389">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7fd76-1390">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-1391">Az.Automation</span></span>
* <span data-ttu-id="7fd76-1392">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7fd76-1393">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7fd76-1394">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1395">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1396">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7fd76-1397">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7fd76-1398">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7fd76-1399">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7fd76-1400">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7fd76-1401">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7fd76-1402">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7fd76-1403">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7fd76-1404">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1405">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1406">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7fd76-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7fd76-1407">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-1408">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-1409">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1410">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-1411">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7fd76-1412">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7fd76-1413">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="7fd76-1414">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7fd76-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7fd76-1415">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7fd76-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7fd76-1416">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7fd76-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7fd76-1417">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7fd76-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1418">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-1419">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="7fd76-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7fd76-1420">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7fd76-1421">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7fd76-1422">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="7fd76-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7fd76-1423">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7fd76-1424">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7fd76-1425">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7fd76-1426">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7fd76-1427">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7fd76-1428">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7fd76-1429">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7fd76-1430">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7fd76-1431">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="7fd76-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7fd76-1432">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7fd76-1433">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7fd76-1434">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7fd76-1435">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7fd76-1436">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7fd76-1437">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7fd76-1438">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1438">Overall improved help files</span></span>
* <span data-ttu-id="7fd76-1439">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1440">Az.Network</span></span>
* <span data-ttu-id="7fd76-1441">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="7fd76-1442">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7fd76-1443">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="7fd76-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7fd76-1444">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7fd76-1445">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="7fd76-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7fd76-1446">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7fd76-1447">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7fd76-1448">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7fd76-1449">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7fd76-1450">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7fd76-1451">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7fd76-1452">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="7fd76-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7fd76-1453">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1453">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-1454">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7fd76-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7fd76-1455">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7fd76-1456">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="7fd76-1457">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7fd76-1457">New-VpnSite</span></span>
        - <span data-ttu-id="7fd76-1458">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7fd76-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="7fd76-1459">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="7fd76-1460">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="7fd76-1461">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1463">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7fd76-1464">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1465">Az.Resources</span></span>
* <span data-ttu-id="7fd76-1466">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="7fd76-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-1468">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7fd76-1469">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7fd76-1470">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7fd76-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7fd76-1471">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7fd76-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7fd76-1472">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7fd76-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7fd76-1473">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7fd76-1474">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7fd76-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7fd76-1475">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7fd76-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7fd76-1476">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7fd76-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7fd76-1477">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7fd76-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7fd76-1478">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7fd76-1479">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7fd76-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7fd76-1480">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7fd76-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7fd76-1481">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7fd76-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7fd76-1482">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="7fd76-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7fd76-1483">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="7fd76-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7fd76-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7fd76-1484">Az.SignalR</span></span>
* <span data-ttu-id="7fd76-1485">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1486">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1487">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7fd76-1488">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7fd76-1489">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7fd76-1490">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7fd76-1491">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1492">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1493">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7fd76-1494">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7fd76-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7fd76-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7fd76-1497">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7fd76-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7fd76-1499">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="7fd76-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7fd76-1500">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7fd76-1501">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7fd76-1502">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7fd76-1503">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7fd76-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-1504">Az.Websites</span></span>
* <span data-ttu-id="7fd76-1505">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="7fd76-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7fd76-1506">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7fd76-1507">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7fd76-1508">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7fd76-1509">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-1509">General</span></span>
* <span data-ttu-id="7fd76-1510">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1511">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1512">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7fd76-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7fd76-1513">Az.Aks</span></span>
* <span data-ttu-id="7fd76-1514">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7fd76-1515">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="7fd76-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-1517">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="7fd76-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7fd76-1518">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7fd76-1519">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7fd76-1520">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="7fd76-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7fd76-1521">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7fd76-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-1522">Az.Batch</span></span>
* <span data-ttu-id="7fd76-1523">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-1524">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-1525">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1526">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1527">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7fd76-1528">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7fd76-1529">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7fd76-1530">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7fd76-1531">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7fd76-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7fd76-1532">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7fd76-1533">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7fd76-1534">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1535">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1536">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7fd76-1537">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7fd76-1538">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7fd76-1539">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-1541">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1542">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-1543">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7fd76-1544">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7fd76-1545">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7fd76-1546">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7fd76-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7fd76-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7fd76-1548">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1549">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-1550">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1551">Az.Network</span></span>
* <span data-ttu-id="7fd76-1552">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7fd76-1553">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7fd76-1554">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7fd76-1555">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7fd76-1556">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="7fd76-1557">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7fd76-1558">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-1560">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7fd76-1561">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1561">Added example</span></span>
    - <span data-ttu-id="7fd76-1562">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7fd76-1563">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7fd76-1564">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1566">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1567">Az.Resources</span></span>
* <span data-ttu-id="7fd76-1568">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7fd76-1569">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7fd76-1570">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7fd76-1571">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fd76-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fd76-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="7fd76-1573">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7fd76-1574">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7fd76-1575">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-1577">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7fd76-1578">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7fd76-1579">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7fd76-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7fd76-1580">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="7fd76-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7fd76-1581">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7fd76-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7fd76-1582">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1583">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1584">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1585">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1586">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7fd76-1587">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="7fd76-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7fd76-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7fd76-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7fd76-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7fd76-1590">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="7fd76-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7fd76-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7fd76-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-1592">Az.Websites</span></span>
* <span data-ttu-id="7fd76-1593">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7fd76-1594">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1595">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1596">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7fd76-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7fd76-1598">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-1599">Az.Automation</span></span>
* <span data-ttu-id="7fd76-1600">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-1602">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1603">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1604">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7fd76-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7fd76-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7fd76-1606">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7fd76-1607">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1608">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1609">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7fd76-1610">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1611">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-1612">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7fd76-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7fd76-1613">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-1614">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-1615">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fd76-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fd76-1616">Az.LogicApp</span></span>
* <span data-ttu-id="7fd76-1617">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7fd76-1618">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7fd76-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="7fd76-1620">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1621">Az.Network</span></span>
* <span data-ttu-id="7fd76-1622">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7fd76-1623">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1623">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-1624">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7fd76-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7fd76-1625">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7fd76-1626">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1627">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1628">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1629">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7fd76-1630">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7fd76-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7fd76-1631">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7fd76-1632">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fd76-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7fd76-1633">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7fd76-1634">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7fd76-1635">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7fd76-1636">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7fd76-1637">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7fd76-1638">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="7fd76-1639">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7fd76-1640">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7fd76-1641">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7fd76-1642">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7fd76-1643">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7fd76-1644">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="7fd76-1645">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7fd76-1646">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7fd76-1647">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7fd76-1648">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7fd76-1649">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7fd76-1650">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-1652">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="7fd76-1653">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1655">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7fd76-1656">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7fd76-1657">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7fd76-1658">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7fd76-1659">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7fd76-1660">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7fd76-1661">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7fd76-1662">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7fd76-1663">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7fd76-1664">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1665">Az.Resources</span></span>
- <span data-ttu-id="7fd76-1666">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7fd76-1667">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fd76-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fd76-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="7fd76-1669">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7fd76-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7fd76-1670">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1671">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1672">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7fd76-1673">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7fd76-1674">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1675">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1676">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7fd76-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7fd76-1677">Az.StorageSync</span></span>
* <span data-ttu-id="7fd76-1678">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7fd76-1679">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-1680">Az.Websites</span></span>
* <span data-ttu-id="7fd76-1681">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="7fd76-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7fd76-1682">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7fd76-1683">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7fd76-1684">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1685">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1686">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7fd76-1687">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7fd76-1688">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7fd76-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1689">Az.Advisor</span></span>
* <span data-ttu-id="7fd76-1690">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7fd76-1691">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-1693">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="7fd76-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7fd76-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7fd76-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7fd76-1695">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7fd76-1696">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7fd76-1697">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="7fd76-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7fd76-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7fd76-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7fd76-1699">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-1700">Az.Automation</span></span>
* <span data-ttu-id="7fd76-1701">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1702">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1703">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-1704">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-1705">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fd76-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fd76-1706">Az.EventGrid</span></span>
* <span data-ttu-id="7fd76-1707">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1708">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-1709">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1710">Az.Network</span></span>
* <span data-ttu-id="7fd76-1711">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7fd76-1712">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-1714">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7fd76-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7fd76-1715">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7fd76-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-1717">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1719">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="7fd76-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1720">Az.Resources</span></span>
    - <span data-ttu-id="7fd76-1721">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7fd76-1722">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7fd76-1723">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7fd76-1724">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fd76-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fd76-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="7fd76-1726">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="7fd76-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1727">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1728">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7fd76-1729">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7fd76-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7fd76-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7fd76-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7fd76-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7fd76-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7fd76-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7fd76-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7fd76-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7fd76-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7fd76-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7fd76-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7fd76-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7fd76-1736">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1737">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1738">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7fd76-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7fd76-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7fd76-1740">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7fd76-1741">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7fd76-1742">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7fd76-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7fd76-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7fd76-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7fd76-1745">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="7fd76-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7fd76-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7fd76-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7fd76-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7fd76-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7fd76-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7fd76-1748">Az.StorageSync</span></span>
* <span data-ttu-id="7fd76-1749">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7fd76-1750">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-1751">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-1752">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7fd76-1753">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7fd76-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7fd76-1754">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7fd76-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7fd76-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7fd76-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7fd76-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1757">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1758">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7fd76-1759">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7fd76-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7fd76-1760">Az.Dns</span></span>
* <span data-ttu-id="7fd76-1761">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fd76-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fd76-1762">Az.EventGrid</span></span>
* <span data-ttu-id="7fd76-1763">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7fd76-1764">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1764">New cmdlets:</span></span>
    - <span data-ttu-id="7fd76-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7fd76-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7fd76-1766">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7fd76-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7fd76-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7fd76-1768">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7fd76-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7fd76-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7fd76-1770">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7fd76-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7fd76-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7fd76-1772">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7fd76-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7fd76-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7fd76-1774">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7fd76-1775">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7fd76-1776">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7fd76-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7fd76-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7fd76-1778">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="7fd76-1779">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7fd76-1780">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7fd76-1781">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="7fd76-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7fd76-1783">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7fd76-1784">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7fd76-1785">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7fd76-1786">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7fd76-1787">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="7fd76-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7fd76-1788">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="7fd76-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7fd76-1789">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7fd76-1790">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="7fd76-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7fd76-1792">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7fd76-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7fd76-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7fd76-1794">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7fd76-1795">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7fd76-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7fd76-1798">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7fd76-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7fd76-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7fd76-1800">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1801">Az.Network</span></span>
* <span data-ttu-id="7fd76-1802">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7fd76-1803">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1803">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7fd76-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7fd76-1805">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7fd76-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7fd76-1806">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1806">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7fd76-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7fd76-1808">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7fd76-1809">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1809">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7fd76-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7fd76-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7fd76-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7fd76-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7fd76-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7fd76-1815">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7fd76-1816">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-1816">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7fd76-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7fd76-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7fd76-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7fd76-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7fd76-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7fd76-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7fd76-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7fd76-1821">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7fd76-1822">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="7fd76-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7fd76-1823">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="7fd76-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7fd76-1824">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7fd76-1825">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7fd76-1826">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7fd76-1827">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7fd76-1828">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="7fd76-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7fd76-1829">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7fd76-1830">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7fd76-1831">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7fd76-1832">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7fd76-1833">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7fd76-1834">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7fd76-1835">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7fd76-1836">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7fd76-1837">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7fd76-1838">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7fd76-1839">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="7fd76-1840">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="7fd76-1841">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7fd76-1842">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7fd76-1843">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-1845">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fd76-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1846">Az.Resources</span></span>
* <span data-ttu-id="7fd76-1847">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7fd76-1848">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7fd76-1849">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7fd76-1850">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-1852">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1853">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1854">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7fd76-1855">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7fd76-1856">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7fd76-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7fd76-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7fd76-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7fd76-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7fd76-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7fd76-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7fd76-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7fd76-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7fd76-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7fd76-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-1862">Az.Storage</span></span>
* <span data-ttu-id="7fd76-1863">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="7fd76-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7fd76-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="7fd76-1865">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="7fd76-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7fd76-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-1867">Az.Websites</span></span>
* <span data-ttu-id="7fd76-1868">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="7fd76-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7fd76-1869">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7fd76-1870">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7fd76-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-1871">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-1872">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1873">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1874">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7fd76-1875">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7fd76-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-1876">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-1877">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="7fd76-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7fd76-1878">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="7fd76-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1879">Az.Network</span></span>
* <span data-ttu-id="7fd76-1880">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7fd76-1881">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-1883">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="7fd76-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-1885">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fd76-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fd76-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="7fd76-1887">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="7fd76-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-1889">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7fd76-1890">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1891">Az.Sql</span></span>
* <span data-ttu-id="7fd76-1892">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7fd76-1893">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7fd76-1894">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7fd76-1895">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="7fd76-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-1896">Az.Websites</span></span>
* <span data-ttu-id="7fd76-1897">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7fd76-1898">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7fd76-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-1900">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7fd76-1901">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7fd76-1902">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7fd76-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7fd76-1903">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="7fd76-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7fd76-1904">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7fd76-1905">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="7fd76-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7fd76-1906">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7fd76-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7fd76-1907">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7fd76-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7fd76-1908">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7fd76-1909">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="7fd76-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7fd76-1910">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="7fd76-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7fd76-1911">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="7fd76-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7fd76-1912">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="7fd76-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7fd76-1913">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7fd76-1914">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="7fd76-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7fd76-1915">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="7fd76-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7fd76-1916">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="7fd76-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7fd76-1917">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="7fd76-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7fd76-1918">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="7fd76-1919">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="7fd76-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7fd76-1920">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7fd76-1921">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7fd76-1922">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7fd76-1923">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="7fd76-1924">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7fd76-1925">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7fd76-1926">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7fd76-1927">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7fd76-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7fd76-1928">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7fd76-1929">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7fd76-1930">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="7fd76-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7fd76-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7fd76-1932">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7fd76-1933">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7fd76-1934">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="7fd76-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7fd76-1935">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7fd76-1936">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7fd76-1937">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7fd76-1938">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7fd76-1939">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7fd76-1940">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="7fd76-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7fd76-1941">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7fd76-1942">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7fd76-1943">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7fd76-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="7fd76-1944">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7fd76-1945">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="7fd76-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7fd76-1946">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7fd76-1947">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7fd76-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="7fd76-1948">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7fd76-1949">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7fd76-1950">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="7fd76-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7fd76-1951">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7fd76-1952">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="7fd76-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7fd76-1953">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7fd76-1954">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7fd76-1955">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7fd76-1956">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7fd76-1957">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7fd76-1958">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7fd76-1959">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7fd76-1960">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7fd76-1961">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7fd76-1962">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7fd76-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7fd76-1963">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7fd76-1964">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="7fd76-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7fd76-1965">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7fd76-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7fd76-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7fd76-1967">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7fd76-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7fd76-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7fd76-1969">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7fd76-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7fd76-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7fd76-1971">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7fd76-1972">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7fd76-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7fd76-1974">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="7fd76-1975">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7fd76-1976">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7fd76-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-1977">Az.Automation</span></span>
* <span data-ttu-id="7fd76-1978">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7fd76-1979">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="7fd76-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7fd76-1980">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="7fd76-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7fd76-1981">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="7fd76-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7fd76-1982">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="7fd76-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7fd76-1983">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7fd76-1984">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="7fd76-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-1985">Az.Compute</span></span>
* <span data-ttu-id="7fd76-1986">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7fd76-1987">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-1989">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="7fd76-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-1990">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-1991">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="7fd76-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-1992">Az.Network</span></span>
* <span data-ttu-id="7fd76-1993">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7fd76-1994">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7fd76-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="7fd76-1995">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7fd76-1996">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7fd76-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-1997">Az.Resources</span></span>
* <span data-ttu-id="7fd76-1998">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-1999">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2000">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fd76-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7fd76-2001">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2002">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2003">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-2005">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="7fd76-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7fd76-2006">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="7fd76-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2007">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2008">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7fd76-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7fd76-2009">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7fd76-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7fd76-2010">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7fd76-2011">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7fd76-2012">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7fd76-2013">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="7fd76-2014">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2014">Breaking changes</span></span>
    - <span data-ttu-id="7fd76-2015">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7fd76-2016">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7fd76-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7fd76-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="7fd76-2018">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7fd76-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7fd76-2019">Az.Dns</span></span>
* <span data-ttu-id="7fd76-2020">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="7fd76-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7fd76-2021">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7fd76-2022">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="7fd76-2024">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7fd76-2025">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-2026">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-2027">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7fd76-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7fd76-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7fd76-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7fd76-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7fd76-2030">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7fd76-2031">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7fd76-2032">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7fd76-2033">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-2034">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-2035">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="7fd76-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7fd76-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7fd76-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7fd76-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7fd76-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7fd76-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7fd76-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7fd76-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7fd76-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7fd76-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7fd76-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7fd76-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7fd76-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7fd76-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7fd76-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7fd76-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7fd76-2047">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="7fd76-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7fd76-2048">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2049">Az.Network</span></span>
* <span data-ttu-id="7fd76-2050">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7fd76-2051">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-2051">New cmdlets</span></span>
        - <span data-ttu-id="7fd76-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="7fd76-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7fd76-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7fd76-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7fd76-2056">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="7fd76-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7fd76-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7fd76-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7fd76-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7fd76-2059">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7fd76-2060">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7fd76-2061">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-2063">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="7fd76-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7fd76-2064">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7fd76-2065">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="7fd76-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-2067">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="7fd76-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7fd76-2068">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="7fd76-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7fd76-2069">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="7fd76-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7fd76-2070">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="7fd76-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7fd76-2071">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="7fd76-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7fd76-2072">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7fd76-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7fd76-2073">Az.Relay</span></span>
* <span data-ttu-id="7fd76-2074">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fd76-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fd76-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="7fd76-2076">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2077">Az.Storage</span></span>
* <span data-ttu-id="7fd76-2078">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7fd76-2079">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7fd76-2080">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7fd76-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="7fd76-2082">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7fd76-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7fd76-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7fd76-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2086">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2087">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7fd76-2088">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7fd76-2089">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fd76-2090">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7fd76-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="7fd76-2091">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="7fd76-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="7fd76-2092">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7fd76-2093">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7fd76-2094">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7fd76-2095">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fd76-2096">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7fd76-2097">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2098">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2099">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fd76-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-2100">Az.Batch</span></span>
* <span data-ttu-id="7fd76-2101">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-2102">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-2103">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-2105">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2106">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2107">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7fd76-2108">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fd76-2109">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-2110">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-2111">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-2113">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fd76-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fd76-2114">Az.EventGrid</span></span>
* <span data-ttu-id="7fd76-2115">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-2116">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-2117">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7fd76-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fd76-2118">Az.HDInsight</span></span>
* <span data-ttu-id="7fd76-2119">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-2120">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-2121">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-2122">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-2123">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fd76-2124">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7fd76-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7fd76-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="7fd76-2126">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7fd76-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7fd76-2127">Az.Media</span></span>
* <span data-ttu-id="7fd76-2128">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-2129">Az.Monitor</span></span>
  * <span data-ttu-id="7fd76-2130">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7fd76-2131">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7fd76-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7fd76-2132">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7fd76-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7fd76-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7fd76-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7fd76-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7fd76-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7fd76-2135">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7fd76-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7fd76-2136">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2137">Az.Network</span></span>
* <span data-ttu-id="7fd76-2138">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fd76-2139">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7fd76-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7fd76-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="7fd76-2141">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-2143">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7fd76-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7fd76-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7fd76-2145">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-2147">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fd76-2148">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7fd76-2149">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7fd76-2150">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7fd76-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7fd76-2151">Az.RedisCache</span></span>
* <span data-ttu-id="7fd76-2152">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2153">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2154">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2155">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2156">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7fd76-2157">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fd76-2158">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7fd76-2159">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7fd76-2160">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="7fd76-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7fd76-2161">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="7fd76-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7fd76-2162">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2163">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2164">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7fd76-2165">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fd76-2166">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7fd76-2167">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7fd76-2168">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fd76-2169">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7fd76-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="7fd76-2170">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="7fd76-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="7fd76-2171">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7fd76-2172">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7fd76-2173">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7fd76-2174">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fd76-2175">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7fd76-2176">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2177">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2178">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="7fd76-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fd76-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fd76-2180">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7fd76-2181">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-2182">Az.Automation</span></span>
* <span data-ttu-id="7fd76-2183">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7fd76-2184">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7fd76-2185">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="7fd76-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2186">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2187">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7fd76-2188">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7fd76-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="7fd76-2190">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="7fd76-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-2191">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-2192">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7fd76-2193">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2194">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2195">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7fd76-2196">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7fd76-2197">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="7fd76-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7fd76-2198">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7fd76-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7fd76-2199">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7fd76-2200">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7fd76-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2201">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2202">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2203">Az.Storage</span></span>
* <span data-ttu-id="7fd76-2204">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="7fd76-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7fd76-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fd76-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="7fd76-2206">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="7fd76-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7fd76-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7fd76-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7fd76-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7fd76-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7fd76-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7fd76-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7fd76-2211">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="7fd76-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7fd76-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7fd76-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7fd76-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7fd76-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fd76-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7fd76-2216">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fd76-2217">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7fd76-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="7fd76-2218">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="7fd76-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="7fd76-2219">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7fd76-2220">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7fd76-2221">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7fd76-2222">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fd76-2223">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7fd76-2224">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-2225">Az.Automation</span></span>
* <span data-ttu-id="7fd76-2226">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7fd76-2227">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="7fd76-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="7fd76-2228">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2228">Pre-Post script</span></span>
    * <span data-ttu-id="7fd76-2229">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="7fd76-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2230">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2231">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7fd76-2232">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-2233">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-2234">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2235">Az.Network</span></span>
* <span data-ttu-id="7fd76-2236">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7fd76-2237">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-2239">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7fd76-2240">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2241">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2242">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7fd76-2243">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2244">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2245">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2246">Az.Storage</span></span>
* <span data-ttu-id="7fd76-2247">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7fd76-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7fd76-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7fd76-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7fd76-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7fd76-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7fd76-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7fd76-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7fd76-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2254">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2255">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="7fd76-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="7fd76-2256">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2257">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2258">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7fd76-2259">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-2260">Az.Automation</span></span>
* <span data-ttu-id="7fd76-2261">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="7fd76-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7fd76-2262">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7fd76-2263">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-2264">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-2265">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2266">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2267">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-2268">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-2269">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fd76-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fd76-2270">Az.LogicApp</span></span>
* <span data-ttu-id="7fd76-2271">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2272">Az.Network</span></span>
* <span data-ttu-id="7fd76-2273">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-2275">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7fd76-2276">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="7fd76-2276">SDK Update</span></span>
* <span data-ttu-id="7fd76-2277">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7fd76-2278">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2279">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2280">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7fd76-2281">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7fd76-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7fd76-2282">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7fd76-2283">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7fd76-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7fd76-2284">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7fd76-2285">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7fd76-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2286">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2287">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7fd76-2288">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2289">Az.Storage</span></span>
* <span data-ttu-id="7fd76-2290">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fd76-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7fd76-2291">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7fd76-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fd76-2293">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-2294">Az.Automation</span></span>
* <span data-ttu-id="7fd76-2295">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7fd76-2296">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7fd76-2297">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-2299">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2300">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2301">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7fd76-2302">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7fd76-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7fd76-2303">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7fd76-2304">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-2306">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fd76-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-2307">Az.EventHub</span></span>
* <span data-ttu-id="7fd76-2308">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-2309">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-2310">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fd76-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fd76-2311">Az.LogicApp</span></span>
* <span data-ttu-id="7fd76-2312">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7fd76-2313">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7fd76-2314">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="7fd76-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7fd76-2315">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7fd76-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7fd76-2316">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7fd76-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7fd76-2317">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7fd76-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7fd76-2318">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7fd76-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7fd76-2319">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7fd76-2320">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7fd76-2321">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7fd76-2322">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7fd76-2323">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7fd76-2324">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fd76-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-2325">Az.Monitor</span></span>
* <span data-ttu-id="7fd76-2326">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2327">Az.Network</span></span>
* <span data-ttu-id="7fd76-2328">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fd76-2330">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7fd76-2331">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="7fd76-2332">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2333">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2334">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7fd76-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7fd76-2335">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7fd76-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7fd76-2336">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="7fd76-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7fd76-2337">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2338">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2339">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7fd76-2340">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="7fd76-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2341">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2342">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7fd76-2343">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2344">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2345">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fd76-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="7fd76-2347">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="7fd76-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2348">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2349">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7fd76-2350">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7fd76-2351">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="7fd76-2353">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2354">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2355">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="7fd76-2356">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7fd76-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7fd76-2357">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="7fd76-2358">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7fd76-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2359">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2360">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7fd76-2361">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7fd76-2362">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7fd76-2363">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2364">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2365">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7fd76-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fd76-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fd76-2367">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="7fd76-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fd76-2369">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="7fd76-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7fd76-2370">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2371">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2372">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fd76-2373">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fd76-2374">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7fd76-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7fd76-2375">Az.Aks</span></span>
* <span data-ttu-id="7fd76-2376">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fd76-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-2377">Az.Automation</span></span>
* <span data-ttu-id="7fd76-2378">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7fd76-2379">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fd76-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fd76-2380">Az.Cdn</span></span>
* <span data-ttu-id="7fd76-2381">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2382">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2383">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7fd76-2384">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7fd76-2385">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7fd76-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7fd76-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7fd76-2387">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fd76-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fd76-2388">Az.DataFactory</span></span>
* <span data-ttu-id="7fd76-2389">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-2391">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7fd76-2392">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7fd76-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7fd76-2393">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-2394">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-2395">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fd76-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-2396">Az.KeyVault</span></span>
* <span data-ttu-id="7fd76-2397">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2398">Az.Network</span></span>
* <span data-ttu-id="7fd76-2399">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2400">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2401">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7fd76-2402">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7fd76-2403">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7fd76-2404">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="7fd76-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7fd76-2405">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="7fd76-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7fd76-2406">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7fd76-2407">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7fd76-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-2409">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7fd76-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7fd76-2410">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2410">Fix some error messages.</span></span>
* <span data-ttu-id="7fd76-2411">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7fd76-2412">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7fd76-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7fd76-2413">Az.SignalR</span></span>
* <span data-ttu-id="7fd76-2414">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2415">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2416">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fd76-2417">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7fd76-2418">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="7fd76-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7fd76-2419">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="7fd76-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2420">Az.Storage</span></span>
* <span data-ttu-id="7fd76-2421">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fd76-2422">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7fd76-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7fd76-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7fd76-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7fd76-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7fd76-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7fd76-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="7fd76-2426">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2427">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2428">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fd76-2429">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7fd76-2430">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7fd76-2431">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="7fd76-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fd76-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2432">Az.Accounts</span></span>
* <span data-ttu-id="7fd76-2433">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2434">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2435">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="7fd76-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7fd76-2436">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7fd76-2437">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-2439">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7fd76-2440">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fd76-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fd76-2441">Az.EventGrid</span></span>
* <span data-ttu-id="7fd76-2442">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7fd76-2443">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7fd76-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7fd76-2444">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7fd76-2445">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="7fd76-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7fd76-2446">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7fd76-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7fd76-2447">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7fd76-2448">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7fd76-2449">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="7fd76-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7fd76-2450">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7fd76-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7fd76-2451">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7fd76-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="7fd76-2452">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7fd76-2453">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="7fd76-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fd76-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd76-2454">Az.IotHub</span></span>
* <span data-ttu-id="7fd76-2455">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fd76-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fd76-2456">Az.LogicApp</span></span>
* <span data-ttu-id="7fd76-2457">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="7fd76-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2458">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2459">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7fd76-2460">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7fd76-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7fd76-2461">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7fd76-2462">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7fd76-2463">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="7fd76-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7fd76-2464">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7fd76-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7fd76-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7fd76-2465">Az.SignalR</span></span>
* <span data-ttu-id="7fd76-2466">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2467">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2468">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fd76-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2469">Az.Storage</span></span>
* <span data-ttu-id="7fd76-2470">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7fd76-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fd76-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="7fd76-2472">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="7fd76-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7fd76-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7fd76-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2474">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2475">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7fd76-2476">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7fd76-2477">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7fd76-2478">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-2478">General</span></span>

- <span data-ttu-id="7fd76-2479">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="7fd76-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="7fd76-2480">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="7fd76-2480">Online help for each module</span></span>
- <span data-ttu-id="7fd76-2481">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7fd76-2482">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7fd76-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fd76-2483">Az.Accounts</span></span>
- <span data-ttu-id="7fd76-2484">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="7fd76-2485">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7fd76-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="7fd76-2487">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="7fd76-2487">Fixes for #7002</span></span>
- <span data-ttu-id="7fd76-2488">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7fd76-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fd76-2489">Az.Batch</span></span>
- <span data-ttu-id="7fd76-2490">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7fd76-2491">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7fd76-2492">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7fd76-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7fd76-2493">Az.Billing</span></span>
- <span data-ttu-id="7fd76-2494">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7fd76-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="7fd76-2496">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7fd76-2497">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7fd76-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="7fd76-2499">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7fd76-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7fd76-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7fd76-2501">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="7fd76-2503">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7fd76-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fd76-2504">Az.Monitor</span></span>
- <span data-ttu-id="7fd76-2505">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7fd76-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fd76-2506">Az.KeyVault</span></span>
- <span data-ttu-id="7fd76-2507">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7fd76-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7fd76-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="7fd76-2509">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7fd76-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7fd76-2510">Az.Media</span></span>
- <span data-ttu-id="7fd76-2511">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7fd76-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2512">Az.Network</span></span>
<span data-ttu-id="7fd76-2513">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7fd76-2514">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="7fd76-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fd76-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fd76-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fd76-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fd76-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fd76-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7fd76-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7fd76-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7fd76-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd76-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7fd76-2523">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7fd76-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fd76-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7fd76-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7fd76-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fd76-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7fd76-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7fd76-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7fd76-2529">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7fd76-2530">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7fd76-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7fd76-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7fd76-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7fd76-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7fd76-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7fd76-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7fd76-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7fd76-2534">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7fd76-2535">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7fd76-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="7fd76-2537">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7fd76-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2538">Az.Profile</span></span>
- <span data-ttu-id="7fd76-2539">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="7fd76-2541">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7fd76-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2542">Az.Resources</span></span>
- <span data-ttu-id="7fd76-2543">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7fd76-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="7fd76-2545">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="7fd76-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7fd76-2546">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7fd76-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7fd76-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="7fd76-2548">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7fd76-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7fd76-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2549">Az.Sql</span></span>
- <span data-ttu-id="7fd76-2550">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7fd76-2551">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7fd76-2552">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7fd76-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2553">Az.Storage</span></span>
- <span data-ttu-id="7fd76-2554">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7fd76-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2555">Az.Websites</span></span>
- <span data-ttu-id="7fd76-2556">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7fd76-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7fd76-2557">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7fd76-2558">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-2558">General</span></span>

* <span data-ttu-id="7fd76-2559">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="7fd76-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7fd76-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2560">Az.Compute</span></span>

* <span data-ttu-id="7fd76-2561">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="7fd76-2563">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7fd76-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fd76-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="7fd76-2565">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="7fd76-2566">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7fd76-2567">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7fd76-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="7fd76-2569">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7fd76-2570">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7fd76-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2571">Az.Resources</span></span>

* <span data-ttu-id="7fd76-2572">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7fd76-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7fd76-2573">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7fd76-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2574">Az.Sql</span></span>

* <span data-ttu-id="7fd76-2575">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="7fd76-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7fd76-2576">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7fd76-2577">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7fd76-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2578">Az.Storage</span></span>

* <span data-ttu-id="7fd76-2579">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7fd76-2580">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7fd76-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7fd76-2582">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="7fd76-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7fd76-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7fd76-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7fd76-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7fd76-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2585">Az.Websites</span></span>

* <span data-ttu-id="7fd76-2586">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd76-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="7fd76-2587">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7fd76-2588">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7fd76-2589">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7fd76-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fd76-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="7fd76-2591">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7fd76-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fd76-2592">Az.Automation</span></span>
* <span data-ttu-id="7fd76-2593">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fd76-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7fd76-2594">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7fd76-2595">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7fd76-2596">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7fd76-2597">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7fd76-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2598">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2599">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7fd76-2600">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7fd76-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="7fd76-2602">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7fd76-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7fd76-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7fd76-2604">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7fd76-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2605">Az.Network</span></span>
* <span data-ttu-id="7fd76-2606">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7fd76-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7fd76-2607">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7fd76-2608">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="7fd76-2609">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7fd76-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7fd76-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7fd76-2611">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7fd76-2612">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7fd76-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7fd76-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7fd76-2614">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="7fd76-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7fd76-2615">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7fd76-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7fd76-2616">Az.Relay</span></span>
* <span data-ttu-id="7fd76-2617">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7fd76-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2618">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2619">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7fd76-2620">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7fd76-2621">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7fd76-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7fd76-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-2623">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7fd76-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2624">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2625">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7fd76-2626">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fd76-2627">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fd76-2628">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fd76-2629">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7fd76-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fd76-2630">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7fd76-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7fd76-2631">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7fd76-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7fd76-2632">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7fd76-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7fd76-2633">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7fd76-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7fd76-2634">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7fd76-2635">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fd76-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7fd76-2636">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7fd76-2637">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="7fd76-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7fd76-2638">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="7fd76-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7fd76-2639">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7fd76-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7fd76-2640">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7fd76-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7fd76-2641">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7fd76-2642">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7fd76-2643">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7fd76-2643">General</span></span>
* <span data-ttu-id="7fd76-2644">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7fd76-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2645">Az.Profile</span></span>
* <span data-ttu-id="7fd76-2646">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7fd76-2647">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7fd76-2648">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7fd76-2649">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7fd76-2650">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7fd76-2651">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7fd76-2652">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="7fd76-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-2654">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2655">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2656">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7fd76-2657">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="7fd76-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7fd76-2658">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-2660">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="7fd76-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7fd76-2661">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7fd76-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7fd76-2662">Az.Insights</span></span>
* <span data-ttu-id="7fd76-2663">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7fd76-2664">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7fd76-2665">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7fd76-2666">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2667">Az.Network</span></span>
* <span data-ttu-id="7fd76-2668">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7fd76-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7fd76-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7fd76-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7fd76-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7fd76-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7fd76-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7fd76-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fd76-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7fd76-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7fd76-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fd76-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fd76-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fd76-2676">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2677">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2678">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7fd76-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7fd76-2679">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="7fd76-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fd76-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fd76-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="7fd76-2681">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="7fd76-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fd76-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fd76-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fd76-2683">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7fd76-2684">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7fd76-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7fd76-2685">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7fd76-2686">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="7fd76-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7fd76-2687">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7fd76-2688">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7fd76-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2689">Az.Profile</span></span>
* <span data-ttu-id="7fd76-2690">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7fd76-2691">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2692">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2693">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="7fd76-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7fd76-2694">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fd76-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fd76-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fd76-2696">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7fd76-2697">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7fd76-2698">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7fd76-2699">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7fd76-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2701">Az.Network</span></span>
* <span data-ttu-id="7fd76-2702">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7fd76-2703">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2704">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2705">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7fd76-2706">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7fd76-2707">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7fd76-2708">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2708">Azure.Storage</span></span>
* <span data-ttu-id="7fd76-2709">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7fd76-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7fd76-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7fd76-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7fd76-2712">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7fd76-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7fd76-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fd76-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fd76-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fd76-2715">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fd76-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fd76-2716">Az.Compute</span></span>
* <span data-ttu-id="7fd76-2717">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="7fd76-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7fd76-2718">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7fd76-2719">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7fd76-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7fd76-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7fd76-2721">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fd76-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fd76-2722">Az.Network</span></span>
* <span data-ttu-id="7fd76-2723">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7fd76-2724">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2724">new cmdlets added</span></span>
    - <span data-ttu-id="7fd76-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fd76-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fd76-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fd76-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fd76-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fd76-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7fd76-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fd76-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7fd76-2731">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7fd76-2732">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7fd76-2733">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7fd76-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7fd76-2734">Az.RedisCache</span></span>
* <span data-ttu-id="7fd76-2735">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="7fd76-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7fd76-2736">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fd76-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fd76-2737">Az.Resources</span></span>
* <span data-ttu-id="7fd76-2738">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7fd76-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7fd76-2739">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="7fd76-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fd76-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fd76-2740">Az.Sql</span></span>
* <span data-ttu-id="7fd76-2741">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="7fd76-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fd76-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fd76-2742">Az.Websites</span></span>
* <span data-ttu-id="7fd76-2743">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="7fd76-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7fd76-2744">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="7fd76-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7fd76-2745">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="7fd76-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7fd76-2746">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="7fd76-2746">Initial Release</span></span>
