---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 86413b426db1b17349c6256f9c70f542c6a62a2f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242290"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="37a30-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="37a30-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="37a30-104">4.5.0: August 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-105">Az.Accounts</span></span>
* <span data-ttu-id="37a30-106">„Connect-AzAccount“ wurde aktualisiert und akzeptiert nun den Parameter „MaxContextPopulation“. [Nr. 9865]</span><span class="sxs-lookup"><span data-stu-id="37a30-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="37a30-107">SubscriptionClient-Version auf 2019-06-01 aktualisiert und Anzeigen von Mandantendomänen [Nr. 9838]</span><span class="sxs-lookup"><span data-stu-id="37a30-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="37a30-108">Unterstützung für Informationen des Home- und des managedBy-Mandanten des Abonnements</span><span class="sxs-lookup"><span data-stu-id="37a30-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="37a30-109">Modulname, Versionsinformationen in Telemetriedaten korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="37a30-110">SqlDatabaseDnsSuffix und ServiceManagementUrl angepasst, wenn Umgebungsmetadatenendpunkt inkompatiblen Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="37a30-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="37a30-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37a30-111">Az.Aks</span></span>
* <span data-ttu-id="37a30-112">„ClientIdAndSecret“ bis „ServicePrincipalIdAndSecret“ entfernt und „ClientIdAndSecret“ als Alias festgelegt [Nr. 12381].</span><span class="sxs-lookup"><span data-stu-id="37a30-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="37a30-113">„Get-AzAks“/„New-AzAks“/“Remove-AzAks“/„Set-AzAks“ bis „Get-AzAksCluster“/„New-AzAksCluster“/„Remove-AzAksCluster“/„Set-AzAksCluster“ entfernt und ursprüngliche Cmdlets als Alias festgelegt [Nr. 12373].</span><span class="sxs-lookup"><span data-stu-id="37a30-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-114">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-115">Neues Cmdlet „Add-AzApiManagementApiToGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="37a30-116">Neues Cmdlet „Get-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="37a30-117">Neues Cmdlet „Get-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="37a30-118">Neues Cmdlet „Get-AzApiManagementGatewayKey“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="37a30-119">Neues Cmdlet „New-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="37a30-120">Neues Cmdlet „New-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="37a30-121">Neues Cmdlet „New-AzApiManagementResourceLocationObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="37a30-122">Neues Cmdlet „Remove-AzApiManagementApiFromGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="37a30-123">Neues Cmdlet „Remove-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="37a30-124">Neues Cmdlet „Remove-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="37a30-125">Neues Cmdlet „Update-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="37a30-126">Neuer optionaler Parameter „[-GatewayId]“ zum Cmdlet „Get-AzApiManagementApi“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-128">„Deny“ speziell als NetworkRules-Standardaktion verwendet</span><span class="sxs-lookup"><span data-stu-id="37a30-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-129">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-130">Problem behoben, aufgrund dessen eine Ausnahme ausgelöst wird, wenn Enum.Parse versucht, einen NULL-Wert in Enumerationswerte vom Typ „Enabled“ oder „Disabled“ umzuwandeln [Nr. 12344]</span><span class="sxs-lookup"><span data-stu-id="37a30-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-131">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-132">Unterstützung für das Erstellen eines Clusters mit dem Feature für Verschlüsselung während der Übertragung</span><span class="sxs-lookup"><span data-stu-id="37a30-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="37a30-133">Neuer Parameter „EncryptionInTransit“ zum Cmdlet „New-AzHDInsightCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="37a30-134">Neuer Parameter „EncryptionInTransit“ zum Cmdlet „New-AzHDInsightClusterConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="37a30-135">Unterstützung für das Erstellen eines Clusters mit der Funktion für private Links:</span><span class="sxs-lookup"><span data-stu-id="37a30-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="37a30-136">Neue Parameter „PublicNetworkAccessType“ und „OutboundPublicNetworkAccessType“ zum Cmdlet „New-AzHDInsightCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="37a30-137">Neue Parameter „PublicNetworkAccessType“ und „OutboundPublicNetworkAccessType“ zum Cmdlet „New-AzHDInsightClusterConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="37a30-138">Beim Aufruf von „New-AzHDInsightCluster“ oder „Get-AzHDInsightCluster“ werden Informationen zum virtuellen Netzwerk zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37a30-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-139">Az.Network</span></span>
* <span data-ttu-id="37a30-140">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="37a30-141">Nonbreaking Changes hinzugefügt: PeerAddressType-Funktion für privates Peering in „Remove-AzExpressRouteCircutPeeringConfig“</span><span class="sxs-lookup"><span data-stu-id="37a30-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="37a30-142">Code geändert, um die Groß-/Kleinschreibung für die Parameter „AddressPrefixType“ und „PeerAddressType“ zu ignorieren</span><span class="sxs-lookup"><span data-stu-id="37a30-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="37a30-143">Warnmeldung für „New-AzLoadBalancerFrontendIpConfig“, „New-AzPublicIpAddress“ und „New-AzPublicIpPrefix“ geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-145">Option „-ForceDelete“ für „Remove-AzOperationalInsightsworkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="37a30-146">Neues Cmdlet „Get-AzOperationalInsightsDeletedWorkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="37a30-147">Neues Cmdlet „Restore-AzOperationalInsightsWorkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-149">Ermittlung von Azure Backup-Containern/-Elementen verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-150">Az.Resources</span></span>
* <span data-ttu-id="37a30-151">Eigenschaften „Condition“, „ConditionVersion“ und „Description“ zu „New-AzRoleAssignment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="37a30-152">Dies enthielt alle relevanten Änderungen an den Datenmodellen.</span><span class="sxs-lookup"><span data-stu-id="37a30-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-153">Az.Sql</span></span>
* <span data-ttu-id="37a30-154">Potenzieller Fehler aufgrund der Nichtbeachtung von Groß-/Kleinschreibung beim Servernamen in „New-AzSqlServer“ und „Set-AzSqlServer“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="37a30-155">Fehler behoben, aufgrund dessen in „New-AzSqlDatabaseSecondary“ ein falscher Datenbankname für eine vorhandene Datenbank zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-156">Az.Storage</span></span>
* <span data-ttu-id="37a30-157">Erstellen von Container-/Blob-SAS-Token mit neuer Berechtigung x,t unterstützt</span><span class="sxs-lookup"><span data-stu-id="37a30-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="37a30-158">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="37a30-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="37a30-159">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="37a30-160">Erstellen von Konto-SAS-Token mit neuer Berechtigung x,t,f unterstützt</span><span class="sxs-lookup"><span data-stu-id="37a30-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="37a30-161">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="37a30-162">Abrufen der Nutzung einer einzelnen Dateifreigabe unterstützt</span><span class="sxs-lookup"><span data-stu-id="37a30-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="37a30-163">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="37a30-164">4.4.0 – Juli 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-165">Az.Accounts</span></span>
* <span data-ttu-id="37a30-166">Neues Cmdlet „Invoke-AzRestMethod“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="37a30-167">Ein Problem wurde behoben, das Authentifizierungsfehler in Szenarien mit mehreren Prozessen verursachen konnte, z. B. beim Ausführen mehrerer Azure PowerShell-Cmdlets mithilfe von „Start-Job“ [Nr. 9448].</span><span class="sxs-lookup"><span data-stu-id="37a30-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="37a30-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37a30-168">Az.Aks</span></span>
* <span data-ttu-id="37a30-169">Fehler behoben: „Get-AzAks“ ruft nicht alle Cluster ab [Nr. 12296]</span><span class="sxs-lookup"><span data-stu-id="37a30-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37a30-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37a30-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="37a30-171">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-172">Az.Automation</span></span>
* <span data-ttu-id="37a30-173">Das Problem wurde behoben, dass die Zeichenfolge mit Escapezeichen nicht in das JSON-Objekt konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="37a30-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-174">Az.Compute</span></span>
* <span data-ttu-id="37a30-175">Beim Verwenden von „New-azvmss“ ohne die Imageversion „latest“ wurde eine Warnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-176">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-177">Globale Parameter zu Data Factory hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37a30-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37a30-178">Az.EventGrid</span></span>
* <span data-ttu-id="37a30-179">Zur Verwendung der API-Version 2020-06-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="37a30-180">Neue Funktionen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-180">Added new features:</span></span>
    - <span data-ttu-id="37a30-181">Eingabezuordnung</span><span class="sxs-lookup"><span data-stu-id="37a30-181">Input mapping</span></span>
    - <span data-ttu-id="37a30-182">Schema für Ereignisbereitstellung</span><span class="sxs-lookup"><span data-stu-id="37a30-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="37a30-183">Private Link</span><span class="sxs-lookup"><span data-stu-id="37a30-183">Private Link</span></span>
    - <span data-ttu-id="37a30-184">Cloud Event V10-Schema</span><span class="sxs-lookup"><span data-stu-id="37a30-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="37a30-185">Service Bus-Thema as Ziel</span><span class="sxs-lookup"><span data-stu-id="37a30-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="37a30-186">Azure-Funktion als Ziel</span><span class="sxs-lookup"><span data-stu-id="37a30-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="37a30-187">WebHook-Batchverarbeitung</span><span class="sxs-lookup"><span data-stu-id="37a30-187">WebHook Batching</span></span>
    - <span data-ttu-id="37a30-188">Sicherer Webhook (AAD-Unterstützung)</span><span class="sxs-lookup"><span data-stu-id="37a30-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="37a30-189">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="37a30-189">IpFiltering</span></span>
* <span data-ttu-id="37a30-190">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="37a30-191">„New-AzEventGridSubscription“/„Update-AzEventGridSubscription“:</span><span class="sxs-lookup"><span data-stu-id="37a30-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="37a30-192">Neue optionale Parameter zur Unterstützung der Webhook-Batchverarbeitung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="37a30-193">Neue optionale Parameter zur Unterstützung der Batchverarbeitung gesicherter Webhooks mithilfe von AAD hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="37a30-194">Neue Enumeration für den EndpointType-Parameter hinzufügen, um das Azure-Funktions-und Service Bus-Thema als neue Ziele zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37a30-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="37a30-195">Neuen optionalen Parameter für das Zustellungsschema hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="37a30-196">„New-AzEventGridTopic“/„Update-AzEventGridTopic“ und „New-AzEventGridDomain“/„Update-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="37a30-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="37a30-197">Neue optionale Parameter zur Unterstützung von IpFiltering hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="37a30-198">„New-AzEventGridTopic“/„New-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="37a30-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="37a30-199">Neue optionale Parameter zur Unterstützung von Eingabezuordnung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-200">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-201">Modul zur Verwendung von API 2020-05-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="37a30-202">Unterstützung für private Links für Storage-, Keyvault- und Web App Service-Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-203">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-204">Erstellen eines Clusters mit ADLSGen1/2-Speicher in nationalen Clouds unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-205">Az.Monitor</span></span>
* <span data-ttu-id="37a30-206">Fehler für „Get-AzDiagnosticSetting“ behoben, wenn Metriken oder Protokolle NULL sind [Nr. 12272]</span><span class="sxs-lookup"><span data-stu-id="37a30-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-207">Az.Network</span></span>
* <span data-ttu-id="37a30-208">Austausch von Parametern in VWan-HubVnet-Verbindung-korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="37a30-209">Neue Cmdlets für Sites von virtuellen Azure-Netzwerkgeräten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="37a30-210">„Get-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="37a30-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="37a30-211">„New-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="37a30-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="37a30-212">„Remove-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="37a30-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="37a30-213">„Update-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="37a30-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="37a30-214">„New-AzOffice365PolicyProperty“</span><span class="sxs-lookup"><span data-stu-id="37a30-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="37a30-215">Neue Cmdlets für virtuelle Azure-Netzwerkgeräte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="37a30-216">„Get-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="37a30-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="37a30-217">„New-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="37a30-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="37a30-218">„Remove-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="37a30-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="37a30-219">„Update-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="37a30-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="37a30-220">„Get-AzNetworkVirtualApplianceSku“</span><span class="sxs-lookup"><span data-stu-id="37a30-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="37a30-221">„New-AzVirtualApplianceSkuProperty“</span><span class="sxs-lookup"><span data-stu-id="37a30-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="37a30-222">Onboarding für Application Gateway für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="37a30-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="37a30-223">Onboarding für StorageSync für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="37a30-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="37a30-224">Onboarding für SignalR für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="37a30-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-226">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="37a30-227">Azure Backup hat Cmdlets optimiert, um den Text genauer zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="37a30-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="37a30-228">Azure Backup hat Unterstützung für das Abrufen von MAB-Agent-Aufträgen mithilfe des Cmdlets „Get-AzRecoveryServicesBackupJob“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-229">Az.Resources</span></span>
* <span data-ttu-id="37a30-230">„Save-azresourcegroupdeploymenttemplate“ auf Verwendung des SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="37a30-231">Cmdlet „Unregister-AzResourceProvider“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-232">Az.Sql</span></span>
* <span data-ttu-id="37a30-233">Unterstützung für Dienstprinzipal und Gastbenutzer im Cmdlet „Set-AzSqlInstanceActiveDirectoryAdministrator“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="37a30-234">Problem in Data Classification-Cmdlets behoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="37a30-235">Unterstützung für Azure SQL Managed Instance-Failover hinzugefügt: „Invoke-AzSqlInstanceFailover“</span><span class="sxs-lookup"><span data-stu-id="37a30-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-236">Az.Storage</span></span>
* <span data-ttu-id="37a30-237">Problem behoben, dass UserAgent für einige Datenebenen-Cmdlets nicht hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="37a30-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="37a30-238">Erstellen/Aktualisieren eines Storage-Kontos mit „MinimumTlsVersion“ und „AllowBlobPublicAccess“ unterstützt</span><span class="sxs-lookup"><span data-stu-id="37a30-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="37a30-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="37a30-240">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="37a30-241">Aktivieren/Deaktivieren der Versionsverwaltung für Blobdienst eines Storage-Kontos unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="37a30-242">„Update-AzStorageBlobServiceProperty“</span><span class="sxs-lookup"><span data-stu-id="37a30-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="37a30-243">Auflisten von Blobs mit Blobversionen unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="37a30-244">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="37a30-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="37a30-245">Abrufen/Entfernen einer einzelnen Blob-Momentaufnahme oder Blobversion unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="37a30-246">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="37a30-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="37a30-247">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="37a30-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="37a30-248">Pipeline aus Blobobjekt unterstützen, das aus Azure.Storage.Blobs V12 generiert wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="37a30-249">„Get-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="37a30-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="37a30-250">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="37a30-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="37a30-251">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="37a30-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="37a30-252">„Set-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="37a30-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="37a30-253">„Start-AzStorageBlobCopy“</span><span class="sxs-lookup"><span data-stu-id="37a30-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37a30-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37a30-254">Az.StorageSync</span></span>
* <span data-ttu-id="37a30-255">Neue Version von StorageSync SDK für ApiVersion 2020-03-01 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="37a30-256">Cmdlet „Update Storage Sync Service“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="37a30-257">„Set-AzStorageSyncService“</span><span class="sxs-lookup"><span data-stu-id="37a30-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="37a30-258">„IncomingTrafficPolicy“ und „PrivateEndpointConnections“ zu StorageSyncService-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-259">Az.Websites</span></span>
* <span data-ttu-id="37a30-260">Unterstützung zur Durchführung von Vorgängen für Slots hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="37a30-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="37a30-261">4.3.0 – Juni 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-262">Az.Accounts</span></span>
* <span data-ttu-id="37a30-263">Standardmäßige Unterstützung der Einstellung der Erkennungsumgebung und das Hinzufügen der Umgebung über „Add-AzEnvironment“</span><span class="sxs-lookup"><span data-stu-id="37a30-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="37a30-264">Aktualisieren von vorgeladenen Assemblys [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="37a30-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="37a30-265">Assembly „Azure.Core“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="37a30-266">Fehler behoben, der dazu führen konnte, dass „Connect-AzAccount“ in der Multithread-Ausführung fehlschlägt [#11201]</span><span class="sxs-lookup"><span data-stu-id="37a30-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="37a30-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37a30-267">Az.Aks</span></span>
* <span data-ttu-id="37a30-268">Ersetzen der Verwendung der alten [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) durch Aufrufe der [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials)- und [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)-APIs</span><span class="sxs-lookup"><span data-stu-id="37a30-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-269">Az.Batch</span></span>
* <span data-ttu-id="37a30-270">Az.Batch für die Verwendung der Microsoft.Azure.Management.Batch-SDK-Version auf 11.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="37a30-271">Möglichkeit zum Festlegen der BatchAccount-Identität im Cmdlet „New-AzBatchAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-273">Anzeige von Kontofunktionen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="37a30-274">Ändern von PublicNetworkAccess wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-275">Az.Compute</span></span>
* <span data-ttu-id="37a30-276">Parameter „SimulateEviction“ wurde den Cmdlets „Set-AzVM“ und „Set-AzVmssVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="37a30-277">„Premium_LRS“ wurde zur Argumentvervollständigung des StorageAccountType-Parameters für das Cmdlet „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="37a30-278">Unterstatus zu VMCustomScriptExtension hinzugefügt [#11297]</span><span class="sxs-lookup"><span data-stu-id="37a30-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="37a30-279">„Delete“ wurde zur Argumentvervollständigung des EvictionPolicy-Parameters für die Cmdlets „New-AzVM“ und „New-AzVMConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="37a30-280">Name der neuen VM-Erweiterung für SAP korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-281">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-282">ADF .Net-SDK-Version auf 4.9.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-283">Az.EventHub</span></span>
* <span data-ttu-id="37a30-284">Parameter der verwalteten Identität zu Cmdlets „New-AzEventHubNamespace“ und „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="37a30-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="37a30-285">Az.Functions</span></span>
* <span data-ttu-id="37a30-286">Unterstützung zum Erstellen von PowerShell 7.0- und Java 11-Funktions-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-287">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-288">Listenhosts unterstützt und bestimmte Hosts des HDInsight-Clusters neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="37a30-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="37a30-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="37a30-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="37a30-290">SDK-Version auf 1.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="37a30-291">Unterstützung für Exporteinstellungen und verwaltete Identität hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-292">Az.Monitor</span></span>
* <span data-ttu-id="37a30-293">Eingabeobjektparameter für „Set-AzActivityLogAlert“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="37a30-294">InputObject-Parameter für „Set-AzActionGroup“ korrigiert [#10868]</span><span class="sxs-lookup"><span data-stu-id="37a30-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-295">Az.Network</span></span>
* <span data-ttu-id="37a30-296">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="37a30-297">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="37a30-298">„New-AzFirewallPolicyDnsSetting“</span><span class="sxs-lookup"><span data-stu-id="37a30-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="37a30-299">Unterstützung für Ziel-FQDN in Netzwerkregeln für Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="37a30-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="37a30-300">Unterstützung für Back-End-Adresspool-Vorgänge hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="37a30-301">„New-AzLoadBalancerBackendAddressConfig“</span><span class="sxs-lookup"><span data-stu-id="37a30-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="37a30-302">„New-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="37a30-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="37a30-303">„Set-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="37a30-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="37a30-304">„Remove-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="37a30-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="37a30-305">„Get-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="37a30-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="37a30-306">Namensvalidierung für „New-AzIpGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="37a30-307">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="37a30-308">„New-AzFirewallPolicyThreatIntelWhitelist“</span><span class="sxs-lookup"><span data-stu-id="37a30-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="37a30-309">Folgende Befehle für das Feature aktualisiert: Festlegen/Entfernen von benutzerdefinierten DNS-Servern auf „VirtualWan P2SVpnGateway“.</span><span class="sxs-lookup"><span data-stu-id="37a30-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="37a30-310">„New-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="37a30-311">„Update-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="37a30-312">„Update-AzVpnGateway“ aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="37a30-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="37a30-313">Der optionale Parameter „-BgpPeeringAddress“ wurde hinzugefügt, damit Kunden ihre benutzerdefinierten BGSs angeben können, die auf „VpnGateway“ festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="37a30-314">Neues Cmdlet hinzugefügt, um das Zurücksetzen des Routingstatus einer VirtualHub-Ressource zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="37a30-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="37a30-315">„Reset-AzHubRouter“</span><span class="sxs-lookup"><span data-stu-id="37a30-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="37a30-316">Folgendes wurde basierend auf der aktuellen Swagger-Änderung für die Firewallrichtlinie aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="37a30-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="37a30-317">Namen für „RuleGroup“, „RuleCollectionGroup“ und „RuleType“ geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="37a30-318">Unterstützung für NAT-Regelsammlungen der Firewallrichtlinie zur Unterstützung mehrerer NAT-Regelsammlungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="37a30-319">[Breaking Change] Obligatorischer Parameter „SourceIpGroup“ für „New-AzFirewallPolicyApplicationRule“ und „New-AzFirewallPolicyNetworkRule“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="37a30-320">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="37a30-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="37a30-321">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="37a30-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="37a30-322">[Breaking Change] Obligatorische Parameter entfernt: „TranslatedAddress“, „TranslatedPort“ für „New-AzFirewallPolicyNatRuleCollection“.</span><span class="sxs-lookup"><span data-stu-id="37a30-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="37a30-323">Neue Cmdlets zur Unterstützung von „PrivateLink“ auf Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="37a30-324">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="37a30-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="37a30-325">„Get-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="37a30-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="37a30-326">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="37a30-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="37a30-327">„Set-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="37a30-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="37a30-328">„Remove-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="37a30-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="37a30-329">„New-AzApplicationGatewayPrivateLinkIpConfiguration“</span><span class="sxs-lookup"><span data-stu-id="37a30-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="37a30-330">Neue Cmdlets für untergeordnete Ressource „HubRouteTables“ von „VirtualHub“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="37a30-331">„New-AzVHubRoute“</span><span class="sxs-lookup"><span data-stu-id="37a30-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="37a30-332">„New-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="37a30-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="37a30-333">„Get-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="37a30-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="37a30-334">„Update-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="37a30-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="37a30-335">„Remove-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="37a30-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="37a30-336">Vorhandene Cmdlets aktualisiert, sodass sie den optionalen Eingabeparameter „RoutingConfiguration“ für benutzerdefiniertes Routing in „VirtualWan“ unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37a30-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="37a30-337">„New-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="37a30-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="37a30-338">„Set-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="37a30-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="37a30-339">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="37a30-340">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="37a30-341">„New-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="37a30-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="37a30-342">„Update-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="37a30-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="37a30-343">„New-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="37a30-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="37a30-344">„Update-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="37a30-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-346">Fehler behoben: „PSWorkspace“ implementiert „IOperationalInsightsWorkspace“ nicht [#12135]</span><span class="sxs-lookup"><span data-stu-id="37a30-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="37a30-347">„pergb2018“ wurde dem gültigen Satz des Parameters „Sku“ in „Set-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="37a30-348">Der Alias „FunctionParameters“ für den Parameter „FunctionParameter“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="37a30-349">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="37a30-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="37a30-350">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="37a30-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-352">Azure Backup hat Unterstützung für das Abrufen von MAB-Elementen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="37a30-353">Azure Site Recovery unterstützt Datenträgertyp „StandardSSD_LRS“.</span><span class="sxs-lookup"><span data-stu-id="37a30-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-354">Az.Resources</span></span>
* <span data-ttu-id="37a30-355">„UsageLocation“, „GivenName“, „Surname“, „AccountEnabled“, „MailNickname“, „Mail“ in „PSADUser“ hinzugefügt [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="37a30-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="37a30-356">Problem behoben, dass „-Mail“ für „Get-AzADUser“ nicht funktioniert [#11981]</span><span class="sxs-lookup"><span data-stu-id="37a30-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="37a30-357">Parameter „-ExcludeChangeType“ zu „Get-AzDeploymentWhatIfResult“ und „Get-AzResourceGroupDeploymentWhatIfResult“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="37a30-358">Parameter „-WhatIfExcludeChangeType“ zu „New-AzDeployment“ und „New-AzResourceGroupDeployment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="37a30-359">Cmdlets von „Test-Az\*Deployment“, sodass bessere Fehlermeldungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="37a30-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="37a30-360">Hilfemeldung für Parameter „-Name“ der Cmdlets „deployment create“ und „What-If“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-361">Az.Sql</span></span>
* <span data-ttu-id="37a30-362">Unterstützung für Dienstprinzipal für Cmdlet „Set SQL Server Azure Active Directory Admin“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="37a30-363">Synchronisierungsproblem in Datenklassifizierungs-Cmdlets wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="37a30-364">Suchen von Benutzern nach E-Mail wird für „Set-AzSqlServerActiveDirectoryAdministrator“ unterstützt [#12192]</span><span class="sxs-lookup"><span data-stu-id="37a30-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-365">Az.Storage</span></span>
* <span data-ttu-id="37a30-366">Erstellen eines Speicherkontos mit „RequireInfrastructureEncryption“ wird unterstützt</span><span class="sxs-lookup"><span data-stu-id="37a30-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="37a30-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="37a30-368">Logik zum Laden von „Azure.Core to Az.Accounts“ verschoben</span><span class="sxs-lookup"><span data-stu-id="37a30-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-369">Az.Websites</span></span>
* <span data-ttu-id="37a30-370">Schutz zum Löschen der erstellten Web-App hinzugefügt, wenn die Wiederherstellung in „Restore-AzDeletedWebApp“ fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="37a30-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="37a30-371">„SourceWebApp.Location“ für „New-AzWebApp“ und „New-AzWebAppSlot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="37a30-372">Fehler behoben, der das Ändern von Containereinstellungen in „Set-AzWebApp“ und „Set-AzWebAppSlot“ verhindert hat.</span><span class="sxs-lookup"><span data-stu-id="37a30-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="37a30-373">Fehler beim Abrufen von „SiteConfig“ behoben, wenn „-Name“ für „Get-AzWebApp“ nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="37a30-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="37a30-374">Unterstützung zum Erstellen von ASP für Linux-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="37a30-375">Ausnahmen für den Ressourcengruppen übergreifenden Klonvorgang hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="37a30-376">4.2.0: Juni 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-377">Az.Accounts</span></span>
* <span data-ttu-id="37a30-378">Problem behoben, das unter Umständen dazu geführt hat, dass Az Protokolle in Azure Automation- oder PowerShell-Aufträgen übersprungen hat [Nr. 11492]</span><span class="sxs-lookup"><span data-stu-id="37a30-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37a30-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37a30-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="37a30-380">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-381">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-382">Assemblyversion der Dienstverwaltungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="37a30-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="37a30-383">Az.Billing</span></span>
* <span data-ttu-id="37a30-384">Assemblyversion der Nutzungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-386">Unterstützung des PrivateEndpoint- und des PublicNetworkAccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="37a30-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-387">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-388">Assemblyversion der Data Factory v2-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="37a30-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="37a30-389">Az.DataShare</span></span>
* <span data-ttu-id="37a30-390">Allgemeine Verfügbarkeit des Moduls „Az.DataShare“</span><span class="sxs-lookup"><span data-stu-id="37a30-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="37a30-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="37a30-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="37a30-392">Allgemeine Verfügbarkeit des Moduls „Az.DesktopVirtualization“</span><span class="sxs-lookup"><span data-stu-id="37a30-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-394">SDK auf 0.21.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="37a30-395">Optionale Parameter hinzugefügt zu:</span><span class="sxs-lookup"><span data-stu-id="37a30-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="37a30-396">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="37a30-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="37a30-397">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="37a30-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-399">Beispiel 3 für „Start-AzPolicyComplianceScan“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="37a30-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="37a30-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="37a30-401">Assemblyversion der PowerBI-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="37a30-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="37a30-402">Az.PrivateDns</span></span>
* <span data-ttu-id="37a30-403">Formatierung der ausführlichen Ausgabezeichenfolge für „Remove-AzPrivateDnsRecordSet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-405">Azure Site Recovery-Unterstützung für die Erstellung eines Wiederherstellungsplans für die Replikation zwischen Zonen per XML-Eingabe</span><span class="sxs-lookup"><span data-stu-id="37a30-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="37a30-406">Assemblyversion der SiteRecovery- und Backup-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-407">Az.Resources</span></span>
* <span data-ttu-id="37a30-408">Tail-Parameter zu den Cmdlets „Get-AzDeploymentScriptLog“ und „Save-AzDeploymentScriptLog“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="37a30-409">Die Output-Eigenschaft wurde formatiert und wird nun in der Ausgabe des Cmdlets „Get-AzDeploymentScript“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37a30-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="37a30-410">Parameter „-DeploymentScriptInputObject“ in „-DeploymentScriptObject“ umbenannt</span><span class="sxs-lookup"><span data-stu-id="37a30-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="37a30-411">Fehlender Datei-/Zielname in Cmdlet-Meldungen korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="37a30-412">Assemblyversion der Resource Manager- und Tags-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-413">Az.Sql</span></span>
* <span data-ttu-id="37a30-414">„UsePrivateLinkConnection“ zu „New-AzSqlSyncGroup“, „Update-AzSqlSyncGroup“, „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="37a30-415">„SyncMemberAzureDatabaseResourceId“ zu „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="37a30-416">Unterstützung für die Gastbenutzersuche zum SQL Server-Cmdlet für den Azure Active Directory-Administrator hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-417">Az.Storage</span></span>
* <span data-ttu-id="37a30-418">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="37a30-419">4.1.0 – Mai 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="37a30-420">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="37a30-420">Highlights since the last release</span></span>
* <span data-ttu-id="37a30-421">Unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="37a30-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="37a30-422">Allgemeine Verfügbarkeit von Az.Functions</span><span class="sxs-lookup"><span data-stu-id="37a30-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="37a30-423">Veröffentlichung von Hauptversionen von Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources und Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-424">Az.Accounts</span></span>
* <span data-ttu-id="37a30-425">„Add-AzEnvironment“ und „Set-AzEnvironment“ akzeptieren jetzt die Parameter „AzureSynapseAnalyticsEndpointResourceId“ und „AzureSynapseAnalyticsEndpointSuffix“.</span><span class="sxs-lookup"><span data-stu-id="37a30-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="37a30-426">Assemblys zu Azure.Core wurden Az.Accounts hinzugefügt. Unterstützte PowerShell-Plattformen sind u. a. Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="37a30-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="37a30-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37a30-427">Az.Aks</span></span>
* <span data-ttu-id="37a30-428">API-Version wurde auf 2019-10-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="37a30-429">Unterstützung für die Erstellung von AKS mit einem Windows-Container</span><span class="sxs-lookup"><span data-stu-id="37a30-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="37a30-430">Neu verfügbare Cmdlets: „New-AzAksNodePool“, „Update-AzAksNodePool“, „Remove-AzAksNodePool“, „Get-AzAksNodePool“, „Install-AzAksKubectl“, „Get-AzAksVersion“</span><span class="sxs-lookup"><span data-stu-id="37a30-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-431">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-432">„New-AzApiManagement“ und „Set-AzApiManagement“: Parameter [-AssignIdentity] wurde in [-SystemAssignedIdentity] umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="37a30-433">„New-AzApiManagement“ und „Set-AzApiManagement“: Neuer Parameter hinzugefügt: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="37a30-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="37a30-434">„Get-AzApiManagementProperty“ wurde in „Get-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="37a30-435">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="37a30-436">„New-AzApiManagementProperty“ wurde in „New-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="37a30-437">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="37a30-438">„Set-AzApiManagementProperty“ wurde in „Set-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="37a30-439">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="37a30-440">„Remove-AzApiManagementProperty“ wurde in „Remove-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="37a30-441">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="37a30-442">Neues Cmdlet „Get-AzApiManagementAuthorizationServerClientSecret“ hinzugefügt. „Get-AzApiManagementAuthorizationServer“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="37a30-443">Neues Cmdlet „Get-AzApiManagementNamedValueSecretValue“ hinzugefügt. „Get-AzApiManagementNamedValue“ gibt keinen Geheimniswert zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="37a30-444">Neues Cmdlet „Get-AzApiManagementOpenIdConnectProviderClientSecret“ hinzugefügt. „Get-AzApiManagementOpenIdConnectProvider“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="37a30-445">Neues Cmdlet „Get-AzApiManagementSubscriptionKey“ hinzugefügt. „Get-AzApiManagementSubscription“ gibt keine Abonnementschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="37a30-446">Neues Cmdlet „Get-AzApiManagementTenantAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="37a30-447">Neues Cmdlet „Get-AzApiManagementTenantGitAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantGitAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="37a30-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="37a30-449">Parameter hinzugefügt: „RetentionInDays“, „PublicNetworkAccessForIngestion“, „PublicNetworkAccessForQuery“ für „New-AzApplicationInsights“</span><span class="sxs-lookup"><span data-stu-id="37a30-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="37a30-450">Cmdlet „Update-AzApplicationInsights“ erstellt.</span><span class="sxs-lookup"><span data-stu-id="37a30-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="37a30-451">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="37a30-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-452">Az.Batch</span></span>
* <span data-ttu-id="37a30-453">Az.Batch für die Verwendung der Microsoft.Azure.Batch-SDK-Version 13.0.0 und der Microsoft.Azure.Management.Batch-SDK-Version 9.0.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="37a30-454">Die Möglichkeit zum Auswählen der Art des hinzugefügten Zertifikats mithilfe des neuen Parameters „-CertificateKind“ wurde zu „New-AzBatchCertificate“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="37a30-455">Eigenschaft „ApplicationPackages“ aus „PSApplication“ entfernt, die bislang immer „“ war.</span><span class="sxs-lookup"><span data-stu-id="37a30-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="37a30-456">Die spezifischen Pakete in einer Anwendung können jetzt mit „Get-AzBatchApplicationPackage“ abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="37a30-457">Beispiel: „Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication“</span><span class="sxs-lookup"><span data-stu-id="37a30-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="37a30-458">Beim Erstellen eines Pools mit „New-AzBatchPool“ kann die Eigenschaft „VirtualMachineImageId“ von „PSImageReference“ jetzt nur auf ein Bild in einer Shared Image Gallery verweisen.</span><span class="sxs-lookup"><span data-stu-id="37a30-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="37a30-459">Wenn Sie einen Pool mit „New-AzBatchPool“ erstellen, kann der Pool mit der Eigenschaft „PublicIPAddressConfiguration“ von „PSNetworkConfiguration“ ohne eine öffentliche IP-Adresse bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="37a30-460">Die Eigenschaft „PublicIPs“ von „PSNetworkConfiguration“ wurde ebenfalls in „PSPublicIPAddressConfiguration“ verschoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="37a30-461">Diese Eigenschaft kann nur angegeben werden, wenn „IPAddressProvisioningType“ den Wert „UserManaged“ hat.</span><span class="sxs-lookup"><span data-stu-id="37a30-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-462">Az.Compute</span></span>
* <span data-ttu-id="37a30-463">HostId-Parameter zum Cmdlet „Update-AzVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="37a30-464">Hilfedokumente für die Cmdlets „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVmss“, „Set-AzVMOperatingSystem“ und „Set-AzVmssOsProfile“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="37a30-465">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="37a30-465">Breaking changes</span></span>
    - <span data-ttu-id="37a30-466">Der FilterExpression-Parameter wurde aus dem Cmdlet „Get-AzVMImage“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="37a30-467">Der AssignIdentity-Parameter wurde aus den Cmdlets „New-AzVmssConfig“, „New-AzVMConfig“ und „Update-AzVM“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="37a30-468">AutomaticRepairMaxInstanceRepairsPercent wurde aus den Cmdlets „New-AzVmssConfig“ und „Update-AzVmss“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="37a30-469">Die Eigenschaften AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus und VirtualMachineScaleSetsColocationStatus wurden aus ProximityPlacementGroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="37a30-470">Die Eigenschaft MaxInstanceRepairsPercent wurde aus AutomaticRepairsPolicy entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="37a30-471">Die Typen von AvailabilitySets, VirtualMachines und VirtualMachineScaleSets wurden von IList<SubResource> in IList<SubResourceWithColocationStatus> geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="37a30-472">Die Beschreibung für das Cmdlet „Get-AzVM“ wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="37a30-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-473">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-474">CRUD von Datenfluss-Laufzeiteigenschaften in Managed IR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-475">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-476">Neue Cmdlets zum Erstellen, Aktualisieren, Abrufen und Löschen von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="37a30-477">Hilfs-Cmdlets für die Erstellung von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="37a30-478">Regelmodulverweis auf Front Door-Routingregelobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="37a30-479">Private Link-Parameter zum Front Door-Back-End-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="37a30-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="37a30-480">Az.Functions</span></span>
* <span data-ttu-id="37a30-481">Allgemeine Verfügbarkeit des Moduls „Az.Functions“</span><span class="sxs-lookup"><span data-stu-id="37a30-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-482">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-483">Datenträgerverschlüsselung mit kundenseitig verwalteten Schlüsseln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="37a30-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="37a30-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="37a30-485">Zugriffsrichtlinien verwenden nicht mehr den aktuellen Prinzipal als Standard.</span><span class="sxs-lookup"><span data-stu-id="37a30-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-486">Az.IotHub</span></span>
* <span data-ttu-id="37a30-487">Cmdlet zum Aufrufen einer Abfrage in einem IoT-Hub zum Abrufen von Informationen mithilfe einer SQL-ähnlichen Sprache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="37a30-488">Problem behoben, dass „Add-AzIotHubDevice“ kein Edge-aktiviertes Gerät ohne untergeordnete Geräte erstellen konnte. [#11597]</span><span class="sxs-lookup"><span data-stu-id="37a30-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="37a30-489">Cmdlet zum Generieren eines SAS-Tokens für IoT-Hub, -Gerät oder -Modul hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="37a30-490">Cmdlet zum Aufrufen der Konfigurationsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="37a30-491">Verwalten der automatischen skalierbaren Bereitstellung von IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="37a30-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="37a30-492">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-492">New cmdlets are:</span></span>
    - <span data-ttu-id="37a30-493">„Add-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="37a30-494">„Get-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="37a30-495">„Remove-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="37a30-496">„Set-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="37a30-497">Cmdlet zum Hinzufügen einer IoT Edge-Bereitstellungsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="37a30-498">Cmdlet zum Anwenden des Konfigurationsinhalts auf das angegebene Edge-Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-499">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-500">Zwei Aliase entfernt: „New-AzKeyVaultCertificateAdministratorDetails“ und „New-AzKeyVaultCertificateOrganizationDetails“</span><span class="sxs-lookup"><span data-stu-id="37a30-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="37a30-501">Vorläufiges Löschen ist beim Erstellen eines Schlüsseltresors standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37a30-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="37a30-502">Netzwerkregeln können so festgelegt werden, dass der Zugriff von bestimmten Netzwerkstandorten beim Erstellen eines Schlüsseltresors gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="37a30-503">Unterstützung für BYOK (Bring Your Own Key) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="37a30-504">„Add-AzKeyVaultKey“ unterstützt die Erstellung eines Schlüsselaustauschschlüssels.</span><span class="sxs-lookup"><span data-stu-id="37a30-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="37a30-505">„Get-AzKeyVaultKey“ unterstützt das Herunterladen eines öffentlichen Schlüssels im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="37a30-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="37a30-506">Abschnitt „KeyOps“ der Hilfedokumentation zu „Add-AzKeyVaultKey“ wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-507">Az.Monitor</span></span>
* <span data-ttu-id="37a30-508">Fehler bei „Set-AzDiagnosticSettings“ behoben. Aufbewahrungsrichtlinie gilt nicht für alle Kategorien. [#11589]</span><span class="sxs-lookup"><span data-stu-id="37a30-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="37a30-509">WebTest-Verfügbarkeitskriterien für die Metrikwarnung V2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="37a30-510">„New-AzMetricAlertRuleV2Criteria“: Option zum Erstellen der Webtest-Verfügbarkeitskriterien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="37a30-511">„Add-AzMetricAlertRuleV2“: Neue Webtest-Verfügbarkeitskriterien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="37a30-512">Redundante Definition für „RetentionPolicy“ in PSLogProfile entfernt. [#7608]</span><span class="sxs-lookup"><span data-stu-id="37a30-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="37a30-513">Redundante in PSEventData definierte Eigenschaften entfernt. [#11353]</span><span class="sxs-lookup"><span data-stu-id="37a30-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="37a30-514">„Get-AzLog“ in „Get-AzActivityLog“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-515">Az.Network</span></span>
* <span data-ttu-id="37a30-516">Breaking Change-Attribut hinzugefügt als Benachrichtigung, dass sich das Standardverhalten der Zone ändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="37a30-517">„New-AzPublicIpAddress“</span><span class="sxs-lookup"><span data-stu-id="37a30-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="37a30-518">„New-AzPublicIpPrefix“</span><span class="sxs-lookup"><span data-stu-id="37a30-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="37a30-519">„New-AzLoadBalancerFrontendIpConfig“</span><span class="sxs-lookup"><span data-stu-id="37a30-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="37a30-520">Unterstützung für die neue Ressource der obersten Ebene SecurityPartnerProvider hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="37a30-521">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-521">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-522">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="37a30-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="37a30-523">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="37a30-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="37a30-524">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="37a30-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="37a30-525">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="37a30-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="37a30-526">„RequiredZoneNames“ für „PSPrivateLinkResource“ und „GroupId“ für „PSPrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="37a30-527">Falscher Typ des Parameters SuccessThresholdRoundTripTimeMs für New-AzNetworkWatcherConnectionMonitorTestConfigurationObject korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="37a30-528">VirtualWan-Cmdlets aktualisiert, sodass der Standardwert des Arguments AllowVnetToVnetTraffic auf True festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="37a30-529">„New-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="37a30-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="37a30-530">„Update-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="37a30-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="37a30-531">Neue Cmdlets zur Unterstützung der DNS-Zonengruppe für den privaten Endpunkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="37a30-532">„New-AzPrivateDnsZoneConfig“</span><span class="sxs-lookup"><span data-stu-id="37a30-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="37a30-533">„Get-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="37a30-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="37a30-534">„New-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="37a30-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="37a30-535">„Set-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="37a30-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="37a30-536">„Remove-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="37a30-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="37a30-537">Parameter „DNSEnableProxy“, „DNSRequireProxyForNetworkRules“ und „DNSServers“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="37a30-538">Parameter „EnableDnsProxy“, „DnsProxyNotRequiredForNetworkRule“ und „DnsServer“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="37a30-539">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37a30-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="37a30-540">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="37a30-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-542">Legacycode zum Anwenden des neuen generierten SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="37a30-543">Cmdlets aufgrund von veralteten APIs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="37a30-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="37a30-544">„Get-AzOperationalInsightsSavedSearchResult“ (alias „Get-AzOperationalInsightsSavedSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="37a30-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="37a30-545">„Get-AzOperationalInsightsSearchResult“ (alias „Get-AzOperationalInsightsSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="37a30-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="37a30-546">„Get-AzOperationalInsightsLinkTarget“ (alias „Get-AzOperationalInsightsLinkTargets“)</span><span class="sxs-lookup"><span data-stu-id="37a30-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="37a30-547">Parameter für „Set-AzOperationalInsightsWorkspace“ und „New-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="37a30-548">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="37a30-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="37a30-549">Cmdlets für Cluster und verknüpften Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="37a30-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-551">Azure Site Recovery: Unterstützung für den Schutz von virtuellen Computern der Näherungsplatzierungsgruppe für den Azure-zu-Azure-Anbieter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="37a30-552">Azure Site Recovery: Unterstützung für die Replikation zwischen Zonen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="37a30-553">Azure Backup: Unterstützung für die langfristige Aufbewahrung von Azure FileShare-Wiederherstellungspunkten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="37a30-554">Azure Backup: Eigenschaften für den Ausschluss von Datenträgern zur Ausgabe des Cmdlet „Get-AzRecoveryServicesBackupItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="37a30-555">Privater Endpunkt für Tresoranmeldeinformationen für den Site Recovery-Dienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-556">Az.Resources</span></span>
* <span data-ttu-id="37a30-557">Warnmeldung zur verzögerten Ansicht beim Erstellen einer neuen Rollendefinition hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="37a30-558">Richtlinien-Cmdlets geändert, sodass sie stark typisierte Objekte ausgeben.</span><span class="sxs-lookup"><span data-stu-id="37a30-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="37a30-559">Parameter „-TenantLevel“ zum Cmdlet „Get-AzResourceLock“ hinzugefügt. [#11335]</span><span class="sxs-lookup"><span data-stu-id="37a30-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="37a30-560">„Remove-AzResourceGroup -Id ResourceId“ korrigiert. [#9882]</span><span class="sxs-lookup"><span data-stu-id="37a30-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="37a30-561">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Ressourcengruppenbereich hinzugefügt: „Get-AzDeploymentResourceGroupWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="37a30-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="37a30-562">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Abonnementbereich hinzugefügt: „Get-AzDeploymentWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="37a30-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="37a30-563">Alias: „Get-AzSubscriptionDeploymentWhatIf“</span><span class="sxs-lookup"><span data-stu-id="37a30-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="37a30-564">Parameter „-WhatIf“ und „-Confirm“ für „New-AzDeployment“ und „New-AzResourceGroupDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben.</span><span class="sxs-lookup"><span data-stu-id="37a30-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="37a30-565">Meldung zur Einstellung der Unterstützung für „ApiVersion“ in Bereitstellungs-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="37a30-566">Funktion zum Anzeigen verbesserter Fehlermeldungen für Bereitstellungsfehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="37a30-567">Protokollierung von correlationId bei Bereitstellungsfehlern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="37a30-568">Eigenschaft „error“ zur Bereitstellungsskriptausgabe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="37a30-569">NuGet-Microsoft.Azure.Management.ResourceManager auf „3.7.1-preview“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="37a30-570">Bestimmte Testfälle entfernt, da die Error-Eigenschaft in DeploymentValidateResult von NuGet 3.7.1-preview in schreibgeschützt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="37a30-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="37a30-571">GenericResourceExpanded aus dem SDK ResourceManager 3.7.1-preview importiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="37a30-572">Tagunterstützung für alle Get-Cmdlets für die Bereitstellung hinzugefügt sowie</span><span class="sxs-lookup"><span data-stu-id="37a30-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="37a30-573">„New-AzDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="37a30-574">„New-AzManagementGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="37a30-575">„New-AzResourceGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="37a30-576">„New-AzTenantDeployment“</span><span class="sxs-lookup"><span data-stu-id="37a30-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-578">Fehler beim Hinzufügen eines Zertifikats mithilfe von „--SecretIdentifier“ behoben, der den falschen Zertifikatfingerabdruck erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="37a30-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-579">Az.Sql</span></span>
* <span data-ttu-id="37a30-580">Leistungsoptimierung von:</span><span class="sxs-lookup"><span data-stu-id="37a30-580">Enhance performance of:</span></span>
    - <span data-ttu-id="37a30-581">„Set-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="37a30-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="37a30-582">„Set-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="37a30-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="37a30-583">„Remove-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="37a30-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="37a30-584">„Remove-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="37a30-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="37a30-585">„Enable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="37a30-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="37a30-586">„Enable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="37a30-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="37a30-587">„Disable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="37a30-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="37a30-588">„Disable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="37a30-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="37a30-589">Clientseitige Validierung des Parameters „RetentionDays“ aus dem Cmdlet „Set-AzSqlDatabaseBackupShortTermRetentionPolicy“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="37a30-590">Fehler beim Überwachen eines Speicherkontos in Vnet und Erstellen einer Rolle für den Mitwirkenden an Speicherblobdaten behoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-591">Az.Storage</span></span>
* <span data-ttu-id="37a30-592">„-AsJob“ hinzugefügt, um das Konto für das Cmdlet „Get-AzStorageAccount“ abzurufen/aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="37a30-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="37a30-593">KeyVersion als optional festgelegt, wenn das Speicherkonto mit KeyvaultEncryption aktualisiert wird, um die automatische Schlüsselrotation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37a30-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="37a30-594">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="37a30-595">Fehler beim Entfernen des Azure-Dateiverzeichnisses mit der Pipeline behoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="37a30-596">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="37a30-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="37a30-597">Behoben [#9880]: Definition des DefaultAction-Werts für NetWorkRule in Übereinstimmung mit Swagger geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="37a30-598">„Update-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="37a30-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="37a30-599">„Get-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="37a30-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="37a30-600">Behoben [#11624]: Doppelte Regeln werden beim Hinzufügen von NetworkRules übersprungen, um Serverfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="37a30-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="37a30-601">„Add-AzStorageAccountNetworkRule“</span><span class="sxs-lookup"><span data-stu-id="37a30-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="37a30-602">Microsoft.Azure.Cosmos.Table SDK auf 1.0.7 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="37a30-603">Warnmeldung hinzugefügt, mit der der Benutzer darauf hingewiesen wird, eine erneute Auflistung mit ContinuationToken auszuführen, wenn nur ein Teil der Elemente in der Liste der DataLake Gen2-Elemente zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="37a30-604">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="37a30-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="37a30-605">Unterstützung für das Erstellen oder Aktualisieren eines Speicherkontos mit Active Directory Domain Service-Authentifizierung für Azure Files.</span><span class="sxs-lookup"><span data-stu-id="37a30-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="37a30-606">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="37a30-607">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="37a30-608">Unterstützung für das Hinzufügen und Auflisten von Kerberos-Schlüsseln des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="37a30-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="37a30-609">„New-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="37a30-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="37a30-610">„Get-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="37a30-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="37a30-611">Unterstützung für Failover für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="37a30-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="37a30-612">„Invoke-AzStorageAccountFailover“</span><span class="sxs-lookup"><span data-stu-id="37a30-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="37a30-613">Hilfe zu „Get-AzStorageBlobCopyState“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="37a30-614">Hilfe zu „Get-AzStorageFileCopyState“ und „Start-AzStorageBlobCopy“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="37a30-615">Speicherclientbibliothek v12 in Cmdlets Queue und File integriert.</span><span class="sxs-lookup"><span data-stu-id="37a30-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="37a30-616">Ausgabetyp von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37a30-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="37a30-617">„Get-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="37a30-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="37a30-618">„Remove-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="37a30-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="37a30-619">„Get-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="37a30-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="37a30-620">„Set-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="37a30-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="37a30-621">„Start-AzStorageFileCopy“</span><span class="sxs-lookup"><span data-stu-id="37a30-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="37a30-622">Ausgabetyp von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37a30-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="37a30-623">„New-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="37a30-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="37a30-624">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="37a30-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="37a30-625">Ausgabetyp von CloudFileShare in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37a30-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="37a30-626">„Get-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="37a30-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="37a30-627">„New-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="37a30-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="37a30-628">„Remove-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="37a30-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="37a30-629">Ausgabetyp von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37a30-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="37a30-630">„Set-AzStorageShareQuota“</span><span class="sxs-lookup"><span data-stu-id="37a30-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="37a30-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="37a30-631">Az.TrafficManager</span></span>
* <span data-ttu-id="37a30-632">Falscher Profilname in der ausführlichen Ausgabe von „DisableAzureTrafficManagerEndpoint“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-633">Az.Websites</span></span>
* <span data-ttu-id="37a30-634">Tippfehler in der Hilfe zu „Update-AzWebAppAccessRestrictionConfig“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="37a30-635">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="37a30-636">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="37a30-636">Highlights since the last release</span></span>
* <span data-ttu-id="37a30-637">Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="37a30-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-638">Az.Accounts</span></span>
* <span data-ttu-id="37a30-639">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="37a30-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-640">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-641">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="37a30-642">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-643">Az.Cdn</span></span>
* <span data-ttu-id="37a30-644">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-646">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="37a30-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-647">Az.Compute</span></span>
* <span data-ttu-id="37a30-648">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="37a30-649">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="37a30-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-650">Az.IotHub</span></span>
* <span data-ttu-id="37a30-651">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="37a30-652">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="37a30-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="37a30-653">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="37a30-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="37a30-654">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="37a30-655">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="37a30-656">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="37a30-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="37a30-657">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="37a30-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="37a30-658">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="37a30-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="37a30-659">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-659">New cmdlets are:</span></span>
    - <span data-ttu-id="37a30-660">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="37a30-661">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="37a30-662">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="37a30-663">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="37a30-664">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-665">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-666">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="37a30-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="37a30-667">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="37a30-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="37a30-668">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="37a30-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="37a30-669">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="37a30-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="37a30-670">Az.Maintenance</span></span>
* <span data-ttu-id="37a30-671">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-672">Az.Monitor</span></span>
* <span data-ttu-id="37a30-673">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="37a30-674">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="37a30-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="37a30-675">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="37a30-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="37a30-676">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="37a30-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="37a30-677">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="37a30-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="37a30-678">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="37a30-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="37a30-679">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="37a30-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="37a30-680">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="37a30-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-681">Az.Network</span></span>
* <span data-ttu-id="37a30-682">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="37a30-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="37a30-683">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="37a30-684">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="37a30-685">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="37a30-686">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="37a30-687">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="37a30-688">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="37a30-689">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="37a30-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="37a30-690">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="37a30-691">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="37a30-692">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="37a30-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="37a30-693">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="37a30-694">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="37a30-695">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="37a30-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="37a30-696">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="37a30-697">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-699">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="37a30-700">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-702">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-703">Az.Sql</span></span>
* <span data-ttu-id="37a30-704">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="37a30-705">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="37a30-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-706">Az.Storage</span></span>
* <span data-ttu-id="37a30-707">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="37a30-708">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="37a30-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="37a30-709">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="37a30-710">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="37a30-711">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="37a30-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="37a30-712">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="37a30-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="37a30-713">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="37a30-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="37a30-714">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="37a30-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="37a30-715">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="37a30-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="37a30-716">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="37a30-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="37a30-717">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="37a30-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="37a30-718">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="37a30-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="37a30-719">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="37a30-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="37a30-720">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="37a30-721">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-721">General</span></span>
* <span data-ttu-id="37a30-722">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37a30-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="37a30-723">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="37a30-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="37a30-724">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="37a30-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="37a30-725">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="37a30-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="37a30-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="37a30-726">Az.Billing</span></span>
  - <span data-ttu-id="37a30-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-727">Az.Compute</span></span>
  - <span data-ttu-id="37a30-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="37a30-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="37a30-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-729">Az.EventHub</span></span>
  - <span data-ttu-id="37a30-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-730">Az.IotHub</span></span>
  - <span data-ttu-id="37a30-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-731">Az.KeyVault</span></span>
  - <span data-ttu-id="37a30-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-732">Az.Monitor</span></span>
  - <span data-ttu-id="37a30-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-733">Az.Network</span></span>
  - <span data-ttu-id="37a30-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-734">Az.Resources</span></span>
  - <span data-ttu-id="37a30-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-735">Az.Storage</span></span>
  - <span data-ttu-id="37a30-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-736">Az.Websites</span></span>
* <span data-ttu-id="37a30-737">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="37a30-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="37a30-738">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="37a30-739">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="37a30-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="37a30-740">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-741">Az.Accounts</span></span>
* <span data-ttu-id="37a30-742">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="37a30-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-743">Az.Compute</span></span>
* <span data-ttu-id="37a30-744">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="37a30-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="37a30-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="37a30-746">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="37a30-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="37a30-747">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="37a30-748">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="37a30-748">[#11354]</span></span>
* <span data-ttu-id="37a30-749">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="37a30-750">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="37a30-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="37a30-751">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="37a30-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="37a30-752">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="37a30-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="37a30-753">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="37a30-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="37a30-754">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="37a30-755">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37a30-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="37a30-756">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="37a30-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="37a30-757">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="37a30-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-758">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-759">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="37a30-760">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-762">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="37a30-763">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-764">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-765">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="37a30-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-766">Az.IotHub</span></span>
* <span data-ttu-id="37a30-767">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="37a30-768">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="37a30-769">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="37a30-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="37a30-770">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="37a30-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-771">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-772">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-773">Az.Monitor</span></span>
* <span data-ttu-id="37a30-774">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-775">Az.Network</span></span>
* <span data-ttu-id="37a30-776">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="37a30-777">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="37a30-778">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="37a30-779">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="37a30-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="37a30-780">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="37a30-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="37a30-781">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-783">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="37a30-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-785">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="37a30-786">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="37a30-787">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="37a30-788">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="37a30-789">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="37a30-790">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-791">Az.Resources</span></span>
* <span data-ttu-id="37a30-792">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="37a30-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="37a30-793">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="37a30-794">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="37a30-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="37a30-795">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-795">Added example.</span></span>
* <span data-ttu-id="37a30-796">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="37a30-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="37a30-797">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-798">Az.Sql</span></span>
* <span data-ttu-id="37a30-799">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="37a30-800">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="37a30-801">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="37a30-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="37a30-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="37a30-802">Az.Support</span></span>
* <span data-ttu-id="37a30-803">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="37a30-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-804">Az.Websites</span></span>
* <span data-ttu-id="37a30-805">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="37a30-806">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="37a30-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="37a30-807">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="37a30-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="37a30-808">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="37a30-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="37a30-809">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="37a30-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="37a30-810">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-811">Az.Accounts</span></span>
* <span data-ttu-id="37a30-812">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="37a30-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="37a30-813">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="37a30-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="37a30-814">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-815">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-816">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="37a30-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="37a30-817">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="37a30-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="37a30-818">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="37a30-819">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="37a30-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-821">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-822">Az.IotHub</span></span>
* <span data-ttu-id="37a30-823">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="37a30-824">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="37a30-825">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37a30-826">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37a30-827">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37a30-828">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="37a30-829">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="37a30-830">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="37a30-831">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="37a30-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="37a30-832">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="37a30-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="37a30-833">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="37a30-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="37a30-834">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="37a30-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="37a30-835">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="37a30-836">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="37a30-837">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="37a30-838">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="37a30-839">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="37a30-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="37a30-840">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="37a30-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="37a30-841">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-842">Az.Monitor</span></span>
* <span data-ttu-id="37a30-843">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="37a30-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-844">Az.Network</span></span>
* <span data-ttu-id="37a30-845">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="37a30-846">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="37a30-847">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="37a30-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="37a30-848">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-849">Az.Resources</span></span>
* <span data-ttu-id="37a30-850">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="37a30-851">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="37a30-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="37a30-852">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="37a30-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="37a30-853">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="37a30-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="37a30-854">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="37a30-855">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="37a30-856">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="37a30-857">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="37a30-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="37a30-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37a30-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="37a30-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37a30-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="37a30-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37a30-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="37a30-861">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="37a30-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37a30-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="37a30-863">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="37a30-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-864">Az.Sql</span></span>
* <span data-ttu-id="37a30-865">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="37a30-866">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="37a30-867">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="37a30-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="37a30-868">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="37a30-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="37a30-869">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="37a30-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="37a30-870">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="37a30-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="37a30-871">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="37a30-872">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="37a30-873">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="37a30-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-874">Az.Storage</span></span>
* <span data-ttu-id="37a30-875">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="37a30-876">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="37a30-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="37a30-877">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="37a30-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="37a30-878">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="37a30-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="37a30-879">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="37a30-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-880">Az.Websites</span></span>
* <span data-ttu-id="37a30-881">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="37a30-882">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="37a30-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="37a30-883">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="37a30-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="37a30-884">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="37a30-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="37a30-885">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="37a30-886">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37a30-887">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="37a30-887">Highlights since the last major release</span></span>
* <span data-ttu-id="37a30-888">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="37a30-889">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="37a30-890">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-891">Az.Accounts</span></span>
* <span data-ttu-id="37a30-892">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-893">Az.Automation</span></span>
* <span data-ttu-id="37a30-894">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-896">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="37a30-897">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="37a30-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-898">Az.Compute</span></span>
* <span data-ttu-id="37a30-899">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="37a30-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-900">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-901">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="37a30-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-902">Az.IotHub</span></span>
* <span data-ttu-id="37a30-903">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="37a30-904">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="37a30-905">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37a30-906">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37a30-907">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37a30-908">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="37a30-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-909">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-910">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-911">Az.Monitor</span></span>
* <span data-ttu-id="37a30-912">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="37a30-913">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="37a30-914">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="37a30-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-915">Az.Network</span></span>
* <span data-ttu-id="37a30-916">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="37a30-917">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="37a30-918">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="37a30-919">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="37a30-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="37a30-920">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-920">No new cmdlets are added.</span></span> <span data-ttu-id="37a30-921">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="37a30-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-923">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-924">Az.Resources</span></span>
* <span data-ttu-id="37a30-925">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="37a30-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="37a30-926">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="37a30-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="37a30-927">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="37a30-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="37a30-928">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="37a30-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="37a30-929">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="37a30-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="37a30-930">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="37a30-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="37a30-931">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="37a30-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="37a30-932">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="37a30-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-933">Az.Sql</span></span>
* <span data-ttu-id="37a30-934">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="37a30-935">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="37a30-936">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="37a30-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="37a30-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="37a30-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="37a30-938">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37a30-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37a30-939">Az.StorageSync</span></span>
* <span data-ttu-id="37a30-940">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="37a30-941">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37a30-942">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="37a30-942">Highlights since the last major release</span></span>
* <span data-ttu-id="37a30-943">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="37a30-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="37a30-944">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-945">Az.Accounts</span></span>
* <span data-ttu-id="37a30-946">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="37a30-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="37a30-947">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="37a30-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-948">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-949">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="37a30-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="37a30-950">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="37a30-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="37a30-951">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="37a30-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="37a30-952">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="37a30-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-953">Az.Compute</span></span>
* <span data-ttu-id="37a30-954">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="37a30-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="37a30-955">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="37a30-956">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="37a30-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="37a30-958">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-959">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-960">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="37a30-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="37a30-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="37a30-962">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="37a30-963">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-964">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-965">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-966">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-967">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="37a30-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-968">Az.Network</span></span>
* <span data-ttu-id="37a30-969">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="37a30-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="37a30-970">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="37a30-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="37a30-971">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="37a30-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="37a30-972">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="37a30-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="37a30-973">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="37a30-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="37a30-974">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="37a30-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="37a30-975">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="37a30-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="37a30-976">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="37a30-977">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-977">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="37a30-979">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="37a30-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37a30-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="37a30-981">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-983">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37a30-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="37a30-984">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="37a30-985">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="37a30-986">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-988">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="37a30-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="37a30-989">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-990">Az.Resources</span></span>
* <span data-ttu-id="37a30-991">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="37a30-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="37a30-992">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-993">Az.Sql</span></span>
<span data-ttu-id="37a30-994">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="37a30-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-995">Az.Storage</span></span>
* <span data-ttu-id="37a30-996">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="37a30-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="37a30-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="37a30-998">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="37a30-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="37a30-999">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1000">Az.Websites</span></span>
* <span data-ttu-id="37a30-1001">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="37a30-1002">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="37a30-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="37a30-1003">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="37a30-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1004">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1005">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="37a30-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-1006">Az.Cdn</span></span>
* <span data-ttu-id="37a30-1007">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="37a30-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1008">Az.Compute</span></span>
* <span data-ttu-id="37a30-1009">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="37a30-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="37a30-1011">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="37a30-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="37a30-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="37a30-1013">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37a30-1014">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="37a30-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="37a30-1015">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37a30-1016">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="37a30-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="37a30-1017">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37a30-1018">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="37a30-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="37a30-1019">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37a30-1020">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="37a30-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="37a30-1021">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="37a30-1022">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="37a30-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="37a30-1023">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="37a30-1024">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="37a30-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="37a30-1025">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="37a30-1026">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="37a30-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="37a30-1027">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="37a30-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="37a30-1028">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="37a30-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="37a30-1029">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="37a30-1030">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="37a30-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1031">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1032">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="37a30-1033">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="37a30-1034">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="37a30-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="37a30-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="37a30-1036">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1037">Az.EventHub</span></span>
* <span data-ttu-id="37a30-1038">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-1039">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-1040">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="37a30-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="37a30-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="37a30-1042">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37a30-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="37a30-1043">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37a30-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="37a30-1044">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="37a30-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="37a30-1045">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37a30-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="37a30-1046">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37a30-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="37a30-1047">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37a30-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="37a30-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="37a30-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="37a30-1049">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="37a30-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1050">Az.Network</span></span>
* <span data-ttu-id="37a30-1051">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="37a30-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1053">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="37a30-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="37a30-1054">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="37a30-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="37a30-1055">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="37a30-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="37a30-1056">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="37a30-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1057">Az.Resources</span></span>
* <span data-ttu-id="37a30-1058">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1059">Az.Sql</span></span>
* <span data-ttu-id="37a30-1060">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="37a30-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="37a30-1061">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="37a30-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="37a30-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="37a30-1063">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1064">Az.Storage</span></span>
* <span data-ttu-id="37a30-1065">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="37a30-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="37a30-1066">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="37a30-1067">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="37a30-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="37a30-1068">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="37a30-1069">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="37a30-1070">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-1070">General</span></span>
* <span data-ttu-id="37a30-1071">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1072">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1073">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="37a30-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="37a30-1074">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="37a30-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-1075">Az.Batch</span></span>
* <span data-ttu-id="37a30-1076">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1077">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1078">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-1080">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="37a30-1081">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="37a30-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="37a30-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="37a30-1083">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="37a30-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-1084">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-1085">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="37a30-1086">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="37a30-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="37a30-1087">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-1088">Az.Monitor</span></span>
* <span data-ttu-id="37a30-1089">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="37a30-1090">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="37a30-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="37a30-1091">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="37a30-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1092">Az.Network</span></span>
* <span data-ttu-id="37a30-1093">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="37a30-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1094">Az.Resources</span></span>
* <span data-ttu-id="37a30-1095">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="37a30-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="37a30-1096">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="37a30-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1097">Az.Sql</span></span>
* <span data-ttu-id="37a30-1098">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1099">Az.Storage</span></span>
* <span data-ttu-id="37a30-1100">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="37a30-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="37a30-1101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="37a30-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="37a30-1103">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="37a30-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="37a30-1104">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="37a30-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="37a30-1105">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="37a30-1106">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="37a30-1107">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="37a30-1108">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="37a30-1109">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="37a30-1110">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="37a30-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="37a30-1111">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="37a30-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="37a30-1112">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="37a30-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="37a30-1113">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37a30-1114">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="37a30-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="37a30-1115">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="37a30-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="37a30-1116">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="37a30-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1117">Az.Compute</span></span>
* <span data-ttu-id="37a30-1118">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="37a30-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="37a30-1119">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="37a30-1120">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="37a30-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="37a30-1121">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37a30-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="37a30-1122">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="37a30-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="37a30-1123">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="37a30-1124">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="37a30-1125">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="37a30-1126">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="37a30-1127">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="37a30-1128">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="37a30-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="37a30-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="37a30-1130">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="37a30-1131">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="37a30-1131">Get the Order</span></span>
* <span data-ttu-id="37a30-1132">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="37a30-1133">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="37a30-1133">Create new Order</span></span>
* <span data-ttu-id="37a30-1134">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="37a30-1135">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="37a30-1135">Remove the Order</span></span>
* <span data-ttu-id="37a30-1136">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="37a30-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="37a30-1137">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="37a30-1137">Now creates Local Share</span></span>
* <span data-ttu-id="37a30-1138">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="37a30-1139">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="37a30-1140">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="37a30-1141">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="37a30-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="37a30-1142">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="37a30-1143">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="37a30-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="37a30-1144">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="37a30-1145">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="37a30-1145">Create new Triggers</span></span>
* <span data-ttu-id="37a30-1146">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="37a30-1147">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="37a30-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1148">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1149">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="37a30-1150">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-1152">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1153">Az.EventHub</span></span>
* <span data-ttu-id="37a30-1154">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-1156">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="37a30-1157">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="37a30-1158">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="37a30-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="37a30-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1160">Az.Network</span></span>
* <span data-ttu-id="37a30-1161">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="37a30-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="37a30-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="37a30-1163">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1165">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="37a30-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="37a30-1166">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="37a30-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="37a30-1167">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="37a30-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37a30-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37a30-1168">Az.RedisCache</span></span>
* <span data-ttu-id="37a30-1169">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="37a30-1170">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="37a30-1171">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1172">Az.Resources</span></span>
- <span data-ttu-id="37a30-1173">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="37a30-1174">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="37a30-1175">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="37a30-1176">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="37a30-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="37a30-1177">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1178">Az.Sql</span></span>
* <span data-ttu-id="37a30-1179">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="37a30-1180">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="37a30-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="37a30-1181">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="37a30-1182">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-1182">General</span></span>
* <span data-ttu-id="37a30-1183">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="37a30-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1184">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1185">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="37a30-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="37a30-1186">Az.Advisor</span></span>
* <span data-ttu-id="37a30-1187">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-1188">Az.Batch</span></span>
* <span data-ttu-id="37a30-1189">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="37a30-1190">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="37a30-1191">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="37a30-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="37a30-1192">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="37a30-1193">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="37a30-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="37a30-1194">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="37a30-1195">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="37a30-1196">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="37a30-1197">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="37a30-1198">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="37a30-1199">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="37a30-1200">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="37a30-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="37a30-1201">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="37a30-1202">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="37a30-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="37a30-1203">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="37a30-1204">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="37a30-1205">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="37a30-1206">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="37a30-1207">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="37a30-1208">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="37a30-1209">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="37a30-1210">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="37a30-1211">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="37a30-1212">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="37a30-1213">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="37a30-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="37a30-1214">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37a30-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="37a30-1215">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="37a30-1216">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="37a30-1217">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="37a30-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="37a30-1218">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="37a30-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="37a30-1219">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="37a30-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="37a30-1220">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="37a30-1221">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="37a30-1222">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="37a30-1223">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="37a30-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="37a30-1224">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="37a30-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-1225">Az.Cdn</span></span>
* <span data-ttu-id="37a30-1226">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="37a30-1227">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1228">Az.Compute</span></span>
* <span data-ttu-id="37a30-1229">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="37a30-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="37a30-1230">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="37a30-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="37a30-1231">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="37a30-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="37a30-1232">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="37a30-1233">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="37a30-1234">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="37a30-1235">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="37a30-1236">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="37a30-1236">Breaking changes</span></span>
    - <span data-ttu-id="37a30-1237">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="37a30-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="37a30-1238">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1239">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1240">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-1242">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="37a30-1243">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="37a30-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="37a30-1244">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="37a30-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="37a30-1245">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="37a30-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="37a30-1246">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="37a30-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="37a30-1247">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="37a30-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-1249">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-1250">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-1251">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="37a30-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="37a30-1252">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="37a30-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="37a30-1253">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="37a30-1254">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="37a30-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="37a30-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="37a30-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="37a30-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="37a30-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="37a30-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="37a30-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37a30-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="37a30-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37a30-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="37a30-1260">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="37a30-1261">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="37a30-1262">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="37a30-1263">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="37a30-1264">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="37a30-1265">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="37a30-1266">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="37a30-1267">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="37a30-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="37a30-1268">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="37a30-1269">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="37a30-1270">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="37a30-1271">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="37a30-1272">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1273">Az.IotHub</span></span>
* <span data-ttu-id="37a30-1274">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="37a30-1274">Breaking changes:</span></span>
    - <span data-ttu-id="37a30-1275">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37a30-1276">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="37a30-1277">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37a30-1278">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="37a30-1279">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="37a30-1280">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="37a30-1281">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="37a30-1282">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="37a30-1283">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37a30-1284">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="37a30-1285">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37a30-1286">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1288">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-1289">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="37a30-1290">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="37a30-1291">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-1292">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-1293">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-1294">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-1295">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-1296">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1297">Az.Resources</span></span>
* <span data-ttu-id="37a30-1298">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1299">Az.Network</span></span>
* <span data-ttu-id="37a30-1300">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="37a30-1301">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37a30-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="37a30-1302">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1303">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1304">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1305">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="37a30-1307">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="37a30-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="37a30-1308">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37a30-1308">New cmdlet:</span></span>
        - <span data-ttu-id="37a30-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="37a30-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="37a30-1310">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="37a30-1311">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="37a30-1312">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="37a30-1313">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="37a30-1314">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="37a30-1315">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="37a30-1316">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="37a30-1317">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="37a30-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="37a30-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="37a30-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="37a30-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="37a30-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="37a30-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="37a30-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="37a30-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="37a30-1323">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="37a30-1324">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37a30-1325">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="37a30-1326">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="37a30-1327">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="37a30-1328">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="37a30-1329">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="37a30-1330">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="37a30-1332">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37a30-1333">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37a30-1334">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37a30-1335">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37a30-1336">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37a30-1337">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="37a30-1338">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="37a30-1339">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="37a30-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="37a30-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="37a30-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="37a30-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="37a30-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="37a30-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="37a30-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="37a30-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="37a30-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="37a30-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="37a30-1346">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37a30-1347">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="37a30-1348">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="37a30-1349">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="37a30-1350">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="37a30-1351">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37a30-1352">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="37a30-1353">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="37a30-1354">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="37a30-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="37a30-1355">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="37a30-1356">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="37a30-1357">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37a30-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="37a30-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37a30-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="37a30-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37a30-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="37a30-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37a30-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-1363">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="37a30-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1364">Az.Sql</span></span>
* <span data-ttu-id="37a30-1365">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="37a30-1366">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="37a30-1367">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="37a30-1368">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="37a30-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="37a30-1369">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="37a30-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="37a30-1370">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="37a30-1371">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="37a30-1372">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="37a30-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="37a30-1373">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1374">Az.Storage</span></span>
* <span data-ttu-id="37a30-1375">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="37a30-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="37a30-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="37a30-1378">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="37a30-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37a30-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="37a30-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37a30-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="37a30-1381">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="37a30-1382">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-1382">General</span></span>
* <span data-ttu-id="37a30-1383">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="37a30-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1384">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1385">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-1387">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="37a30-1388">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="37a30-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-1389">Az.Automation</span></span>
* <span data-ttu-id="37a30-1390">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-1391">Az.Batch</span></span>
* <span data-ttu-id="37a30-1392">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1393">Az.Compute</span></span>
* <span data-ttu-id="37a30-1394">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="37a30-1395">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="37a30-1396">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="37a30-1397">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="37a30-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1398">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1399">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="37a30-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="37a30-1400">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="37a30-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="37a30-1401">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-1403">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="37a30-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="37a30-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="37a30-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="37a30-1405">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="37a30-1406">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="37a30-1407">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="37a30-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="37a30-1408">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1409">Az.IotHub</span></span>
* <span data-ttu-id="37a30-1410">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="37a30-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="37a30-1411">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="37a30-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-1412">Az.Monitor</span></span>
* <span data-ttu-id="37a30-1413">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="37a30-1414">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="37a30-1415">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="37a30-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="37a30-1416">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="37a30-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1417">Az.Network</span></span>
* <span data-ttu-id="37a30-1418">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="37a30-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="37a30-1419">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="37a30-1420">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-1421">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="37a30-1422">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="37a30-1423">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="37a30-1424">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="37a30-1425">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37a30-1426">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37a30-1427">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="37a30-1428">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="37a30-1429">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="37a30-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="37a30-1430">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="37a30-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="37a30-1431">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="37a30-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37a30-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37a30-1432">Az.RedisCache</span></span>
* <span data-ttu-id="37a30-1433">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="37a30-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1434">Az.Sql</span></span>
* <span data-ttu-id="37a30-1435">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1436">Az.Storage</span></span>
* <span data-ttu-id="37a30-1437">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="37a30-1438">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="37a30-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="37a30-1439">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37a30-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="37a30-1440">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="37a30-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="37a30-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37a30-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37a30-1442">Az.StorageSync</span></span>
* <span data-ttu-id="37a30-1443">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1444">Az.Websites</span></span>
* <span data-ttu-id="37a30-1445">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="37a30-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="37a30-1446">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="37a30-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-1448">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="37a30-1449">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="37a30-1450">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-1451">Az.Automation</span></span>
* <span data-ttu-id="37a30-1452">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="37a30-1453">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="37a30-1454">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1455">Az.Compute</span></span>
* <span data-ttu-id="37a30-1456">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="37a30-1457">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="37a30-1458">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="37a30-1459">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="37a30-1460">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="37a30-1461">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="37a30-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="37a30-1462">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="37a30-1463">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="37a30-1464">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1465">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1466">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="37a30-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="37a30-1467">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-1468">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-1469">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1470">Az.IotHub</span></span>
* <span data-ttu-id="37a30-1471">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="37a30-1472">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="37a30-1473">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="37a30-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="37a30-1474">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37a30-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="37a30-1475">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37a30-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="37a30-1476">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37a30-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="37a30-1477">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37a30-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-1478">Az.Monitor</span></span>
* <span data-ttu-id="37a30-1479">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="37a30-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="37a30-1480">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="37a30-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="37a30-1481">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="37a30-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="37a30-1482">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="37a30-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="37a30-1483">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="37a30-1484">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="37a30-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="37a30-1485">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="37a30-1486">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="37a30-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="37a30-1487">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="37a30-1488">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="37a30-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="37a30-1489">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="37a30-1490">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="37a30-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="37a30-1491">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="37a30-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="37a30-1492">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="37a30-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="37a30-1493">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="37a30-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="37a30-1494">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="37a30-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="37a30-1495">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="37a30-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="37a30-1496">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="37a30-1497">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="37a30-1498">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-1498">Overall improved help files</span></span>
* <span data-ttu-id="37a30-1499">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1500">Az.Network</span></span>
* <span data-ttu-id="37a30-1501">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="37a30-1502">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="37a30-1503">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="37a30-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="37a30-1504">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="37a30-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="37a30-1505">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="37a30-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="37a30-1506">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="37a30-1507">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="37a30-1508">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="37a30-1509">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="37a30-1510">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="37a30-1511">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="37a30-1512">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="37a30-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="37a30-1513">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1513">New cmdlets</span></span>
        - <span data-ttu-id="37a30-1514">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="37a30-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="37a30-1515">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="37a30-1516">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37a30-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="37a30-1517">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="37a30-1517">New-VpnSite</span></span>
        - <span data-ttu-id="37a30-1518">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="37a30-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="37a30-1519">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="37a30-1520">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="37a30-1521">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="37a30-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1523">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="37a30-1524">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1525">Az.Resources</span></span>
* <span data-ttu-id="37a30-1526">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="37a30-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-1528">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="37a30-1529">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="37a30-1530">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37a30-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37a30-1531">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="37a30-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="37a30-1532">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="37a30-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="37a30-1533">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="37a30-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="37a30-1534">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37a30-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37a30-1535">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37a30-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37a30-1536">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="37a30-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="37a30-1537">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="37a30-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="37a30-1538">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="37a30-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="37a30-1539">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37a30-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37a30-1540">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="37a30-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="37a30-1541">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="37a30-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="37a30-1542">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="37a30-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="37a30-1543">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="37a30-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="37a30-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="37a30-1544">Az.SignalR</span></span>
* <span data-ttu-id="37a30-1545">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1546">Az.Sql</span></span>
* <span data-ttu-id="37a30-1547">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="37a30-1548">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="37a30-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="37a30-1549">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="37a30-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="37a30-1550">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="37a30-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="37a30-1551">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="37a30-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1552">Az.Storage</span></span>
* <span data-ttu-id="37a30-1553">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="37a30-1554">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="37a30-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37a30-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="37a30-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37a30-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="37a30-1557">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="37a30-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37a30-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="37a30-1559">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="37a30-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="37a30-1560">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="37a30-1561">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="37a30-1562">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="37a30-1563">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37a30-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1564">Az.Websites</span></span>
* <span data-ttu-id="37a30-1565">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="37a30-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="37a30-1566">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="37a30-1567">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="37a30-1568">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="37a30-1569">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-1569">General</span></span>
* <span data-ttu-id="37a30-1570">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1571">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1572">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="37a30-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="37a30-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37a30-1573">Az.Aks</span></span>
* <span data-ttu-id="37a30-1574">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="37a30-1575">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="37a30-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-1577">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="37a30-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="37a30-1578">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="37a30-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="37a30-1579">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="37a30-1580">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="37a30-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="37a30-1581">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="37a30-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-1582">Az.Batch</span></span>
* <span data-ttu-id="37a30-1583">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="37a30-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-1584">Az.Cdn</span></span>
* <span data-ttu-id="37a30-1585">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1586">Az.Compute</span></span>
* <span data-ttu-id="37a30-1587">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="37a30-1588">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="37a30-1589">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="37a30-1590">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="37a30-1591">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="37a30-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="37a30-1592">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="37a30-1593">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="37a30-1594">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1595">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1596">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="37a30-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="37a30-1597">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="37a30-1598">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="37a30-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="37a30-1599">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-1601">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1602">Az.EventHub</span></span>
* <span data-ttu-id="37a30-1603">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="37a30-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="37a30-1604">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="37a30-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="37a30-1605">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="37a30-1606">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="37a30-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="37a30-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="37a30-1608">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-1609">Az.Monitor</span></span>
* <span data-ttu-id="37a30-1610">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1611">Az.Network</span></span>
* <span data-ttu-id="37a30-1612">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="37a30-1613">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="37a30-1614">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="37a30-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="37a30-1615">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="37a30-1616">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="37a30-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="37a30-1617">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="37a30-1618">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="37a30-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-1620">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="37a30-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="37a30-1621">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1621">Added example</span></span>
    - <span data-ttu-id="37a30-1622">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="37a30-1623">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="37a30-1624">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1626">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1627">Az.Resources</span></span>
* <span data-ttu-id="37a30-1628">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="37a30-1629">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="37a30-1630">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="37a30-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="37a30-1631">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37a30-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37a30-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="37a30-1633">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="37a30-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="37a30-1634">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="37a30-1635">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-1637">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="37a30-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="37a30-1638">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="37a30-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="37a30-1639">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="37a30-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="37a30-1640">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="37a30-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="37a30-1641">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="37a30-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="37a30-1642">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="37a30-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1643">Az.Sql</span></span>
* <span data-ttu-id="37a30-1644">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1645">Az.Storage</span></span>
* <span data-ttu-id="37a30-1646">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="37a30-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="37a30-1647">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="37a30-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="37a30-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37a30-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="37a30-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37a30-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="37a30-1650">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="37a30-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="37a30-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37a30-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1652">Az.Websites</span></span>
* <span data-ttu-id="37a30-1653">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="37a30-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="37a30-1654">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1655">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1656">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="37a30-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="37a30-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="37a30-1658">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-1659">Az.Automation</span></span>
* <span data-ttu-id="37a30-1660">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-1662">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1663">Az.Compute</span></span>
* <span data-ttu-id="37a30-1664">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="37a30-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37a30-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="37a30-1666">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="37a30-1667">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="37a30-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1668">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1669">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="37a30-1670">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1671">Az.EventHub</span></span>
* <span data-ttu-id="37a30-1672">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="37a30-1673">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="37a30-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-1674">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-1675">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37a30-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37a30-1676">Az.LogicApp</span></span>
* <span data-ttu-id="37a30-1677">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="37a30-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="37a30-1678">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="37a30-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="37a30-1680">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1681">Az.Network</span></span>
* <span data-ttu-id="37a30-1682">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="37a30-1683">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1683">New cmdlets</span></span>
        - <span data-ttu-id="37a30-1684">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37a30-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37a30-1685">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37a30-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37a30-1686">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1687">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1688">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1689">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37a30-1690">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="37a30-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="37a30-1691">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37a30-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="37a30-1692">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37a30-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="37a30-1693">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="37a30-1694">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="37a30-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="37a30-1695">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="37a30-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="37a30-1696">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="37a30-1697">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="37a30-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="37a30-1698">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="37a30-1699">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37a30-1700">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37a30-1701">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="37a30-1702">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="37a30-1703">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="37a30-1704">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37a30-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="37a30-1705">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="37a30-1706">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="37a30-1707">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="37a30-1708">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="37a30-1709">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="37a30-1710">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="37a30-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-1712">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="37a30-1713">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1715">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="37a30-1716">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="37a30-1717">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="37a30-1718">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="37a30-1719">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="37a30-1720">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="37a30-1721">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="37a30-1722">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="37a30-1723">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="37a30-1724">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1725">Az.Resources</span></span>
- <span data-ttu-id="37a30-1726">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="37a30-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="37a30-1727">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37a30-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37a30-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="37a30-1729">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="37a30-1730">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="37a30-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1731">Az.Sql</span></span>
* <span data-ttu-id="37a30-1732">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="37a30-1733">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="37a30-1734">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1735">Az.Storage</span></span>
* <span data-ttu-id="37a30-1736">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="37a30-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37a30-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37a30-1737">Az.StorageSync</span></span>
* <span data-ttu-id="37a30-1738">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="37a30-1739">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1740">Az.Websites</span></span>
* <span data-ttu-id="37a30-1741">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="37a30-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="37a30-1742">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="37a30-1743">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="37a30-1744">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1745">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1746">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="37a30-1747">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="37a30-1748">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="37a30-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="37a30-1749">Az.Advisor</span></span>
* <span data-ttu-id="37a30-1750">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="37a30-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="37a30-1751">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="37a30-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37a30-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-1753">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="37a30-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="37a30-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="37a30-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="37a30-1755">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="37a30-1756">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="37a30-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="37a30-1757">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="37a30-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="37a30-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="37a30-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="37a30-1759">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-1760">Az.Automation</span></span>
* <span data-ttu-id="37a30-1761">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1762">Az.Compute</span></span>
* <span data-ttu-id="37a30-1763">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-1764">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-1765">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37a30-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37a30-1766">Az.EventGrid</span></span>
* <span data-ttu-id="37a30-1767">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1768">Az.IotHub</span></span>
* <span data-ttu-id="37a30-1769">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1770">Az.Network</span></span>
* <span data-ttu-id="37a30-1771">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="37a30-1772">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-1774">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="37a30-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="37a30-1775">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="37a30-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-1777">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1779">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="37a30-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1780">Az.Resources</span></span>
    - <span data-ttu-id="37a30-1781">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="37a30-1782">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="37a30-1783">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="37a30-1784">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37a30-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37a30-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="37a30-1786">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="37a30-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1787">Az.Sql</span></span>
* <span data-ttu-id="37a30-1788">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="37a30-1789">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="37a30-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="37a30-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="37a30-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="37a30-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="37a30-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="37a30-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="37a30-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="37a30-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="37a30-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="37a30-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="37a30-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="37a30-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="37a30-1796">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1797">Az.Storage</span></span>
* <span data-ttu-id="37a30-1798">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="37a30-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="37a30-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="37a30-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="37a30-1800">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="37a30-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="37a30-1801">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="37a30-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="37a30-1802">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="37a30-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="37a30-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="37a30-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="37a30-1805">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="37a30-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="37a30-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37a30-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="37a30-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37a30-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37a30-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37a30-1808">Az.StorageSync</span></span>
* <span data-ttu-id="37a30-1809">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="37a30-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="37a30-1810">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-1811">Az.Accounts</span></span>
* <span data-ttu-id="37a30-1812">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="37a30-1813">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="37a30-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="37a30-1814">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="37a30-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="37a30-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="37a30-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="37a30-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1817">Az.Compute</span></span>
* <span data-ttu-id="37a30-1818">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="37a30-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="37a30-1819">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="37a30-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="37a30-1820">Az.Dns</span></span>
* <span data-ttu-id="37a30-1821">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37a30-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37a30-1822">Az.EventGrid</span></span>
* <span data-ttu-id="37a30-1823">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="37a30-1824">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1824">New cmdlets:</span></span>
    - <span data-ttu-id="37a30-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37a30-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="37a30-1826">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="37a30-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="37a30-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37a30-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="37a30-1828">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37a30-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="37a30-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37a30-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="37a30-1830">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="37a30-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="37a30-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="37a30-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="37a30-1832">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="37a30-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="37a30-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="37a30-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="37a30-1834">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="37a30-1835">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="37a30-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="37a30-1836">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="37a30-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="37a30-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="37a30-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="37a30-1838">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37a30-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="37a30-1839">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="37a30-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="37a30-1840">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="37a30-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="37a30-1841">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="37a30-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="37a30-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="37a30-1843">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="37a30-1844">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="37a30-1845">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="37a30-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="37a30-1846">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="37a30-1847">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="37a30-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="37a30-1848">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="37a30-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="37a30-1849">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="37a30-1850">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="37a30-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="37a30-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="37a30-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="37a30-1852">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="37a30-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="37a30-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="37a30-1854">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="37a30-1855">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="37a30-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="37a30-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="37a30-1858">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="37a30-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="37a30-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="37a30-1860">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1861">Az.Network</span></span>
* <span data-ttu-id="37a30-1862">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="37a30-1863">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1863">New cmdlets</span></span>
        - <span data-ttu-id="37a30-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="37a30-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="37a30-1865">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="37a30-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="37a30-1866">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1866">New cmdlets</span></span>
        - <span data-ttu-id="37a30-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="37a30-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="37a30-1868">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="37a30-1869">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1869">New cmdlets</span></span>
        - <span data-ttu-id="37a30-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37a30-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37a30-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37a30-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37a30-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37a30-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37a30-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="37a30-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="37a30-1875">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="37a30-1876">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-1876">New cmdlets</span></span>
        - <span data-ttu-id="37a30-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37a30-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37a30-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37a30-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37a30-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37a30-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37a30-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="37a30-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="37a30-1881">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="37a30-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="37a30-1882">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="37a30-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="37a30-1883">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="37a30-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="37a30-1884">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="37a30-1885">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="37a30-1886">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="37a30-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="37a30-1887">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="37a30-1888">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="37a30-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="37a30-1889">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="37a30-1890">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="37a30-1891">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="37a30-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="37a30-1892">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="37a30-1893">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="37a30-1894">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="37a30-1895">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="37a30-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="37a30-1896">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="37a30-1897">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="37a30-1898">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="37a30-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="37a30-1899">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="37a30-1900">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="37a30-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="37a30-1901">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="37a30-1902">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="37a30-1903">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-1905">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="37a30-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-1906">Az.Resources</span></span>
* <span data-ttu-id="37a30-1907">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="37a30-1908">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="37a30-1909">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="37a30-1910">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="37a30-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-1912">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="37a30-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1913">Az.Sql</span></span>
* <span data-ttu-id="37a30-1914">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="37a30-1915">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="37a30-1916">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="37a30-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37a30-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="37a30-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37a30-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="37a30-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37a30-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="37a30-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="37a30-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="37a30-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="37a30-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-1922">Az.Storage</span></span>
* <span data-ttu-id="37a30-1923">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="37a30-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="37a30-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="37a30-1925">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="37a30-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="37a30-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1927">Az.Websites</span></span>
* <span data-ttu-id="37a30-1928">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="37a30-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="37a30-1929">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="37a30-1930">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="37a30-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-1931">Az.Cdn</span></span>
* <span data-ttu-id="37a30-1932">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37a30-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-1933">Az.Compute</span></span>
* <span data-ttu-id="37a30-1934">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="37a30-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="37a30-1935">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="37a30-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-1936">Az.EventHub</span></span>
* <span data-ttu-id="37a30-1937">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="37a30-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="37a30-1938">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="37a30-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-1939">Az.Network</span></span>
* <span data-ttu-id="37a30-1940">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="37a30-1941">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-1943">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="37a30-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-1945">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37a30-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37a30-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="37a30-1947">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="37a30-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-1949">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="37a30-1950">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-1951">Az.Sql</span></span>
* <span data-ttu-id="37a30-1952">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="37a30-1953">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="37a30-1954">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="37a30-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="37a30-1955">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="37a30-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-1956">Az.Websites</span></span>
* <span data-ttu-id="37a30-1957">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="37a30-1958">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="37a30-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-1960">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="37a30-1961">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="37a30-1962">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="37a30-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="37a30-1963">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="37a30-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="37a30-1964">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="37a30-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="37a30-1965">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="37a30-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="37a30-1966">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="37a30-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="37a30-1967">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="37a30-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="37a30-1968">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="37a30-1969">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="37a30-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="37a30-1970">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="37a30-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="37a30-1971">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="37a30-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="37a30-1972">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="37a30-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="37a30-1973">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="37a30-1974">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="37a30-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="37a30-1975">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="37a30-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="37a30-1976">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="37a30-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="37a30-1977">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="37a30-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="37a30-1978">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="37a30-1979">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="37a30-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="37a30-1980">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="37a30-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="37a30-1981">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="37a30-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="37a30-1982">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="37a30-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="37a30-1983">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="37a30-1984">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="37a30-1985">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="37a30-1986">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="37a30-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="37a30-1987">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="37a30-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="37a30-1988">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="37a30-1989">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="37a30-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="37a30-1990">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="37a30-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="37a30-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="37a30-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="37a30-1992">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="37a30-1993">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="37a30-1994">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="37a30-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="37a30-1995">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="37a30-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="37a30-1996">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="37a30-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="37a30-1997">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="37a30-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="37a30-1998">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="37a30-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="37a30-1999">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="37a30-2000">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="37a30-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="37a30-2001">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="37a30-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="37a30-2002">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="37a30-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="37a30-2003">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="37a30-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="37a30-2004">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="37a30-2005">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="37a30-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="37a30-2006">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="37a30-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="37a30-2007">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="37a30-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="37a30-2008">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="37a30-2009">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="37a30-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="37a30-2010">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="37a30-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="37a30-2011">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="37a30-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="37a30-2012">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="37a30-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="37a30-2013">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="37a30-2014">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="37a30-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="37a30-2015">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="37a30-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="37a30-2016">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="37a30-2017">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="37a30-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="37a30-2018">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="37a30-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="37a30-2019">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="37a30-2020">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="37a30-2021">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="37a30-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="37a30-2022">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="37a30-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="37a30-2023">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="37a30-2024">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="37a30-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="37a30-2025">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="37a30-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="37a30-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="37a30-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="37a30-2027">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="37a30-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="37a30-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="37a30-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="37a30-2029">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="37a30-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="37a30-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="37a30-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="37a30-2031">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="37a30-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="37a30-2032">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="37a30-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="37a30-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="37a30-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="37a30-2034">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="37a30-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="37a30-2035">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="37a30-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="37a30-2036">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="37a30-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2037">Az.Automation</span></span>
* <span data-ttu-id="37a30-2038">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="37a30-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="37a30-2039">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="37a30-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="37a30-2040">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="37a30-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="37a30-2041">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="37a30-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="37a30-2042">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="37a30-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="37a30-2043">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="37a30-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="37a30-2044">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="37a30-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2045">Az.Compute</span></span>
* <span data-ttu-id="37a30-2046">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="37a30-2047">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2049">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="37a30-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-2050">Az.Monitor</span></span>
* <span data-ttu-id="37a30-2051">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="37a30-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2052">Az.Network</span></span>
* <span data-ttu-id="37a30-2053">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="37a30-2054">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37a30-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="37a30-2055">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="37a30-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="37a30-2056">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="37a30-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2057">Az.Resources</span></span>
* <span data-ttu-id="37a30-2058">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2059">Az.Sql</span></span>
* <span data-ttu-id="37a30-2060">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="37a30-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="37a30-2061">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2062">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2063">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="37a30-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-2065">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="37a30-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="37a30-2066">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="37a30-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2067">Az.Compute</span></span>
* <span data-ttu-id="37a30-2068">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="37a30-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="37a30-2069">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="37a30-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="37a30-2070">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="37a30-2071">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="37a30-2072">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="37a30-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="37a30-2073">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="37a30-2074">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="37a30-2074">Breaking changes</span></span>
    - <span data-ttu-id="37a30-2075">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="37a30-2076">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="37a30-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="37a30-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="37a30-2078">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="37a30-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="37a30-2079">Az.Dns</span></span>
* <span data-ttu-id="37a30-2080">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="37a30-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="37a30-2081">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="37a30-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="37a30-2082">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37a30-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="37a30-2084">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="37a30-2085">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="37a30-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="37a30-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-2086">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-2087">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="37a30-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="37a30-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37a30-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="37a30-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37a30-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="37a30-2090">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="37a30-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="37a30-2091">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="37a30-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="37a30-2092">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="37a30-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="37a30-2093">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="37a30-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-2094">Az.Monitor</span></span>
* <span data-ttu-id="37a30-2095">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="37a30-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="37a30-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="37a30-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="37a30-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="37a30-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="37a30-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="37a30-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="37a30-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="37a30-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="37a30-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="37a30-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="37a30-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="37a30-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="37a30-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37a30-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37a30-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37a30-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37a30-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37a30-2107">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="37a30-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="37a30-2108">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="37a30-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2109">Az.Network</span></span>
* <span data-ttu-id="37a30-2110">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="37a30-2111">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-2111">New cmdlets</span></span>
        - <span data-ttu-id="37a30-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="37a30-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="37a30-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="37a30-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="37a30-2116">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="37a30-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="37a30-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="37a30-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="37a30-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="37a30-2119">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="37a30-2120">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="37a30-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="37a30-2121">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="37a30-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-2123">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="37a30-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="37a30-2124">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="37a30-2125">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="37a30-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-2127">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="37a30-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="37a30-2128">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="37a30-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="37a30-2129">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="37a30-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="37a30-2130">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="37a30-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="37a30-2131">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="37a30-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="37a30-2132">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="37a30-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="37a30-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="37a30-2133">Az.Relay</span></span>
* <span data-ttu-id="37a30-2134">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="37a30-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37a30-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37a30-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="37a30-2136">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2137">Az.Storage</span></span>
* <span data-ttu-id="37a30-2138">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="37a30-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="37a30-2139">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="37a30-2140">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="37a30-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="37a30-2142">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="37a30-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="37a30-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="37a30-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="37a30-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2146">Az.Websites</span></span>
* <span data-ttu-id="37a30-2147">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="37a30-2148">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="37a30-2149">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37a30-2150">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="37a30-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="37a30-2151">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="37a30-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="37a30-2152">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="37a30-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="37a30-2153">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="37a30-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="37a30-2154">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="37a30-2155">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37a30-2156">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="37a30-2157">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2158">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2159">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="37a30-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37a30-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-2160">Az.Batch</span></span>
* <span data-ttu-id="37a30-2161">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-2162">Az.Cdn</span></span>
* <span data-ttu-id="37a30-2163">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-2165">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2166">Az.Compute</span></span>
* <span data-ttu-id="37a30-2167">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="37a30-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="37a30-2168">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37a30-2169">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-2170">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-2171">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="37a30-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2173">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37a30-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37a30-2174">Az.EventGrid</span></span>
* <span data-ttu-id="37a30-2175">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="37a30-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-2176">Az.EventHub</span></span>
* <span data-ttu-id="37a30-2177">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37a30-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37a30-2178">Az.HDInsight</span></span>
* <span data-ttu-id="37a30-2179">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-2180">Az.IotHub</span></span>
* <span data-ttu-id="37a30-2181">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-2182">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-2183">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37a30-2184">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="37a30-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="37a30-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="37a30-2186">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="37a30-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="37a30-2187">Az.Media</span></span>
* <span data-ttu-id="37a30-2188">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-2189">Az.Monitor</span></span>
  * <span data-ttu-id="37a30-2190">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="37a30-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="37a30-2191">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="37a30-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="37a30-2192">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="37a30-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="37a30-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="37a30-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="37a30-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="37a30-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="37a30-2195">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="37a30-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="37a30-2196">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2197">Az.Network</span></span>
* <span data-ttu-id="37a30-2198">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37a30-2199">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="37a30-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="37a30-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="37a30-2201">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-2203">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="37a30-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="37a30-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="37a30-2205">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-2207">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37a30-2208">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="37a30-2209">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="37a30-2210">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37a30-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37a30-2211">Az.RedisCache</span></span>
* <span data-ttu-id="37a30-2212">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2213">Az.Resources</span></span>
* <span data-ttu-id="37a30-2214">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2215">Az.Sql</span></span>
* <span data-ttu-id="37a30-2216">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="37a30-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="37a30-2217">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37a30-2218">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="37a30-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="37a30-2219">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="37a30-2220">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="37a30-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="37a30-2221">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="37a30-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="37a30-2222">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2223">Az.Websites</span></span>
* <span data-ttu-id="37a30-2224">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="37a30-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="37a30-2225">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="37a30-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37a30-2226">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="37a30-2227">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="37a30-2228">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37a30-2229">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="37a30-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="37a30-2230">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="37a30-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="37a30-2231">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="37a30-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="37a30-2232">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="37a30-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="37a30-2233">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="37a30-2234">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37a30-2235">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="37a30-2236">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37a30-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2237">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2238">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="37a30-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37a30-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="37a30-2240">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="37a30-2241">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="37a30-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2242">Az.Automation</span></span>
* <span data-ttu-id="37a30-2243">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="37a30-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="37a30-2244">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="37a30-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="37a30-2245">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="37a30-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2246">Az.Compute</span></span>
* <span data-ttu-id="37a30-2247">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="37a30-2248">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="37a30-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="37a30-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="37a30-2250">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="37a30-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-2251">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-2252">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="37a30-2253">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2254">Az.Resources</span></span>
* <span data-ttu-id="37a30-2255">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="37a30-2256">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="37a30-2257">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="37a30-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="37a30-2258">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="37a30-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="37a30-2259">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="37a30-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="37a30-2260">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="37a30-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2261">Az.Sql</span></span>
* <span data-ttu-id="37a30-2262">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="37a30-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2263">Az.Storage</span></span>
* <span data-ttu-id="37a30-2264">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="37a30-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="37a30-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="37a30-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="37a30-2266">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="37a30-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="37a30-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="37a30-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="37a30-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="37a30-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="37a30-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="37a30-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="37a30-2271">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="37a30-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="37a30-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37a30-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="37a30-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37a30-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="37a30-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37a30-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="37a30-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37a30-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="37a30-2276">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37a30-2277">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="37a30-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="37a30-2278">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="37a30-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="37a30-2279">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="37a30-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="37a30-2280">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="37a30-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="37a30-2281">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="37a30-2282">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37a30-2283">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="37a30-2284">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2285">Az.Automation</span></span>
* <span data-ttu-id="37a30-2286">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="37a30-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="37a30-2287">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="37a30-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="37a30-2288">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="37a30-2288">Pre-Post script</span></span>
    * <span data-ttu-id="37a30-2289">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="37a30-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2290">Az.Compute</span></span>
* <span data-ttu-id="37a30-2291">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="37a30-2292">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-2293">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-2294">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2295">Az.Network</span></span>
* <span data-ttu-id="37a30-2296">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="37a30-2297">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-2299">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="37a30-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="37a30-2300">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2301">Az.Resources</span></span>
* <span data-ttu-id="37a30-2302">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="37a30-2303">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="37a30-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2304">Az.Sql</span></span>
* <span data-ttu-id="37a30-2305">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37a30-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2306">Az.Storage</span></span>
* <span data-ttu-id="37a30-2307">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="37a30-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="37a30-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="37a30-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37a30-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="37a30-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="37a30-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="37a30-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="37a30-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="37a30-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2314">Az.Websites</span></span>
* <span data-ttu-id="37a30-2315">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="37a30-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="37a30-2316">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2317">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2318">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37a30-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="37a30-2319">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2320">Az.Automation</span></span>
* <span data-ttu-id="37a30-2321">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="37a30-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="37a30-2322">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="37a30-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="37a30-2323">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37a30-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-2324">Az.Cdn</span></span>
* <span data-ttu-id="37a30-2325">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="37a30-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2326">Az.Compute</span></span>
* <span data-ttu-id="37a30-2327">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-2328">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-2329">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37a30-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37a30-2330">Az.LogicApp</span></span>
* <span data-ttu-id="37a30-2331">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="37a30-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2332">Az.Network</span></span>
* <span data-ttu-id="37a30-2333">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-2335">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="37a30-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="37a30-2336">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="37a30-2336">SDK Update</span></span>
* <span data-ttu-id="37a30-2337">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="37a30-2338">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2339">Az.Resources</span></span>
* <span data-ttu-id="37a30-2340">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="37a30-2341">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="37a30-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="37a30-2342">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="37a30-2343">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="37a30-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="37a30-2344">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="37a30-2345">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="37a30-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2346">Az.Sql</span></span>
* <span data-ttu-id="37a30-2347">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="37a30-2348">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2349">Az.Storage</span></span>
* <span data-ttu-id="37a30-2350">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a30-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="37a30-2351">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="37a30-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="37a30-2353">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2354">Az.Automation</span></span>
* <span data-ttu-id="37a30-2355">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="37a30-2356">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="37a30-2357">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="37a30-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-2359">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2360">Az.Compute</span></span>
* <span data-ttu-id="37a30-2361">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="37a30-2362">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="37a30-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="37a30-2363">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="37a30-2364">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="37a30-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2366">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37a30-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37a30-2367">Az.EventHub</span></span>
* <span data-ttu-id="37a30-2368">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-2369">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-2370">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37a30-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37a30-2371">Az.LogicApp</span></span>
* <span data-ttu-id="37a30-2372">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="37a30-2373">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="37a30-2374">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="37a30-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="37a30-2375">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37a30-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="37a30-2376">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37a30-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="37a30-2377">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37a30-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="37a30-2378">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37a30-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="37a30-2379">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="37a30-2380">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="37a30-2381">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="37a30-2382">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="37a30-2383">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="37a30-2384">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37a30-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-2385">Az.Monitor</span></span>
* <span data-ttu-id="37a30-2386">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2387">Az.Network</span></span>
* <span data-ttu-id="37a30-2388">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="37a30-2390">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="37a30-2391">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="37a30-2392">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="37a30-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2393">Az.Resources</span></span>
* <span data-ttu-id="37a30-2394">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="37a30-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="37a30-2395">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="37a30-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="37a30-2396">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="37a30-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="37a30-2397">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="37a30-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2398">Az.Sql</span></span>
* <span data-ttu-id="37a30-2399">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="37a30-2400">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="37a30-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2401">Az.Websites</span></span>
* <span data-ttu-id="37a30-2402">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="37a30-2403">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2404">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2405">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="37a30-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37a30-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="37a30-2407">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="37a30-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2408">Az.Compute</span></span>
* <span data-ttu-id="37a30-2409">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="37a30-2410">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="37a30-2411">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="37a30-2413">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="37a30-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2414">Az.Resources</span></span>
* <span data-ttu-id="37a30-2415">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="37a30-2416">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="37a30-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="37a30-2417">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="37a30-2418">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="37a30-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2419">Az.Sql</span></span>
* <span data-ttu-id="37a30-2420">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="37a30-2421">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="37a30-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="37a30-2422">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="37a30-2423">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2424">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2425">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="37a30-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37a30-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="37a30-2427">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="37a30-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="37a30-2429">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="37a30-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="37a30-2430">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2431">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2432">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37a30-2433">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37a30-2434">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="37a30-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37a30-2435">Az.Aks</span></span>
* <span data-ttu-id="37a30-2436">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37a30-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2437">Az.Automation</span></span>
* <span data-ttu-id="37a30-2438">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="37a30-2439">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37a30-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37a30-2440">Az.Cdn</span></span>
* <span data-ttu-id="37a30-2441">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2442">Az.Compute</span></span>
* <span data-ttu-id="37a30-2443">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="37a30-2444">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="37a30-2445">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="37a30-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37a30-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="37a30-2447">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37a30-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a30-2448">Az.DataFactory</span></span>
* <span data-ttu-id="37a30-2449">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2451">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="37a30-2452">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="37a30-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="37a30-2453">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-2454">Az.IotHub</span></span>
* <span data-ttu-id="37a30-2455">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37a30-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-2456">Az.KeyVault</span></span>
* <span data-ttu-id="37a30-2457">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2458">Az.Network</span></span>
* <span data-ttu-id="37a30-2459">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2460">Az.Resources</span></span>
* <span data-ttu-id="37a30-2461">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="37a30-2462">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="37a30-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="37a30-2463">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="37a30-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="37a30-2464">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="37a30-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="37a30-2465">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="37a30-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="37a30-2466">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="37a30-2467">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="37a30-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-2469">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="37a30-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="37a30-2470">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2470">Fix some error messages.</span></span>
* <span data-ttu-id="37a30-2471">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="37a30-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="37a30-2472">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="37a30-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="37a30-2473">Az.SignalR</span></span>
* <span data-ttu-id="37a30-2474">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2475">Az.Sql</span></span>
* <span data-ttu-id="37a30-2476">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37a30-2477">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="37a30-2478">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="37a30-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="37a30-2479">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="37a30-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2480">Az.Storage</span></span>
* <span data-ttu-id="37a30-2481">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37a30-2482">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="37a30-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="37a30-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="37a30-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="37a30-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="37a30-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="37a30-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="37a30-2486">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2487">Az.Websites</span></span>
* <span data-ttu-id="37a30-2488">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37a30-2489">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="37a30-2490">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="37a30-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="37a30-2491">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="37a30-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37a30-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2492">Az.Accounts</span></span>
* <span data-ttu-id="37a30-2493">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2494">Az.Compute</span></span>
* <span data-ttu-id="37a30-2495">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="37a30-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="37a30-2496">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="37a30-2497">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2499">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="37a30-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="37a30-2500">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37a30-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37a30-2501">Az.EventGrid</span></span>
* <span data-ttu-id="37a30-2502">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="37a30-2503">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="37a30-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="37a30-2504">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="37a30-2505">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="37a30-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="37a30-2506">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="37a30-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="37a30-2507">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="37a30-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="37a30-2508">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="37a30-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="37a30-2509">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="37a30-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="37a30-2510">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="37a30-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="37a30-2511">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="37a30-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="37a30-2512">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="37a30-2513">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="37a30-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37a30-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37a30-2514">Az.IotHub</span></span>
* <span data-ttu-id="37a30-2515">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37a30-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37a30-2516">Az.LogicApp</span></span>
* <span data-ttu-id="37a30-2517">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="37a30-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2518">Az.Resources</span></span>
* <span data-ttu-id="37a30-2519">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="37a30-2520">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="37a30-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="37a30-2521">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="37a30-2522">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="37a30-2523">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="37a30-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="37a30-2524">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="37a30-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="37a30-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="37a30-2525">Az.SignalR</span></span>
* <span data-ttu-id="37a30-2526">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2527">Az.Sql</span></span>
* <span data-ttu-id="37a30-2528">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37a30-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2529">Az.Storage</span></span>
* <span data-ttu-id="37a30-2530">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="37a30-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="37a30-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="37a30-2532">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="37a30-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="37a30-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="37a30-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2534">Az.Websites</span></span>
* <span data-ttu-id="37a30-2535">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="37a30-2536">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="37a30-2537">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="37a30-2538">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-2538">General</span></span>

- <span data-ttu-id="37a30-2539">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="37a30-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="37a30-2540">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="37a30-2540">Online help for each module</span></span>
- <span data-ttu-id="37a30-2541">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="37a30-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="37a30-2542">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="37a30-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37a30-2543">Az.Accounts</span></span>
- <span data-ttu-id="37a30-2544">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37a30-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="37a30-2545">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="37a30-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="37a30-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="37a30-2547">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="37a30-2547">Fixes for #7002</span></span>
- <span data-ttu-id="37a30-2548">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="37a30-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37a30-2549">Az.Batch</span></span>
- <span data-ttu-id="37a30-2550">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="37a30-2551">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="37a30-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="37a30-2552">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="37a30-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="37a30-2553">Az.Billing</span></span>
- <span data-ttu-id="37a30-2554">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="37a30-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="37a30-2556">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="37a30-2557">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="37a30-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="37a30-2559">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="37a30-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="37a30-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="37a30-2561">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="37a30-2563">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="37a30-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37a30-2564">Az.Monitor</span></span>
- <span data-ttu-id="37a30-2565">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="37a30-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37a30-2566">Az.KeyVault</span></span>
- <span data-ttu-id="37a30-2567">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="37a30-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="37a30-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="37a30-2569">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="37a30-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="37a30-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="37a30-2570">Az.Media</span></span>
- <span data-ttu-id="37a30-2571">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="37a30-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="37a30-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2572">Az.Network</span></span>
<span data-ttu-id="37a30-2573">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="37a30-2574">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="37a30-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37a30-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37a30-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37a30-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37a30-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37a30-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37a30-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="37a30-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37a30-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="37a30-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a30-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="37a30-2583">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="37a30-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37a30-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="37a30-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="37a30-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37a30-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="37a30-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="37a30-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="37a30-2589">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="37a30-2590">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37a30-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="37a30-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37a30-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="37a30-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37a30-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="37a30-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37a30-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="37a30-2594">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="37a30-2595">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="37a30-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="37a30-2597">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="37a30-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37a30-2598">Az.Profile</span></span>
- <span data-ttu-id="37a30-2599">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="37a30-2601">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="37a30-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2602">Az.Resources</span></span>
- <span data-ttu-id="37a30-2603">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="37a30-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="37a30-2605">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="37a30-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="37a30-2606">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="37a30-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="37a30-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="37a30-2608">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="37a30-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="37a30-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2609">Az.Sql</span></span>
- <span data-ttu-id="37a30-2610">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="37a30-2611">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="37a30-2612">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="37a30-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2613">Az.Storage</span></span>
- <span data-ttu-id="37a30-2614">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="37a30-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2615">Az.Websites</span></span>
- <span data-ttu-id="37a30-2616">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="37a30-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="37a30-2617">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="37a30-2618">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-2618">General</span></span>

* <span data-ttu-id="37a30-2619">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="37a30-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="37a30-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2620">Az.Compute</span></span>

* <span data-ttu-id="37a30-2621">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="37a30-2623">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="37a30-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37a30-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="37a30-2625">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="37a30-2626">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="37a30-2627">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="37a30-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="37a30-2629">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="37a30-2630">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="37a30-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="37a30-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2631">Az.Resources</span></span>

* <span data-ttu-id="37a30-2632">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="37a30-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="37a30-2633">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37a30-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="37a30-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2634">Az.Sql</span></span>

* <span data-ttu-id="37a30-2635">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="37a30-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="37a30-2636">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="37a30-2637">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="37a30-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2638">Az.Storage</span></span>

* <span data-ttu-id="37a30-2639">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="37a30-2640">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="37a30-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="37a30-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="37a30-2642">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="37a30-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="37a30-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="37a30-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="37a30-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="37a30-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2645">Az.Websites</span></span>

* <span data-ttu-id="37a30-2646">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37a30-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="37a30-2647">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37a30-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="37a30-2648">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="37a30-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="37a30-2649">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="37a30-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37a30-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="37a30-2651">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="37a30-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37a30-2652">Az.Automation</span></span>
* <span data-ttu-id="37a30-2653">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37a30-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="37a30-2654">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="37a30-2655">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="37a30-2656">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="37a30-2657">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="37a30-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2658">Az.Compute</span></span>
* <span data-ttu-id="37a30-2659">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="37a30-2660">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="37a30-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="37a30-2662">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="37a30-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="37a30-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="37a30-2664">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="37a30-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2665">Az.Network</span></span>
* <span data-ttu-id="37a30-2666">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="37a30-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="37a30-2667">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="37a30-2668">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="37a30-2669">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="37a30-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="37a30-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="37a30-2671">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="37a30-2672">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="37a30-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="37a30-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="37a30-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="37a30-2674">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="37a30-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="37a30-2675">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="37a30-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="37a30-2676">Az.Relay</span></span>
* <span data-ttu-id="37a30-2677">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="37a30-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="37a30-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2678">Az.Resources</span></span>
* <span data-ttu-id="37a30-2679">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="37a30-2680">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="37a30-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="37a30-2681">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="37a30-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="37a30-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-2683">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="37a30-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2684">Az.Sql</span></span>
* <span data-ttu-id="37a30-2685">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="37a30-2686">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37a30-2687">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37a30-2688">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37a30-2689">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37a30-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37a30-2690">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37a30-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="37a30-2691">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37a30-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="37a30-2692">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37a30-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="37a30-2693">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37a30-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="37a30-2694">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="37a30-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="37a30-2695">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="37a30-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="37a30-2696">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="37a30-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="37a30-2697">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="37a30-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="37a30-2698">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="37a30-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="37a30-2699">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="37a30-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="37a30-2700">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="37a30-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="37a30-2701">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="37a30-2702">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="37a30-2703">Allgemein</span><span class="sxs-lookup"><span data-stu-id="37a30-2703">General</span></span>
* <span data-ttu-id="37a30-2704">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="37a30-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="37a30-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37a30-2705">Az.Profile</span></span>
* <span data-ttu-id="37a30-2706">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="37a30-2707">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="37a30-2708">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="37a30-2709">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="37a30-2710">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="37a30-2711">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="37a30-2712">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="37a30-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-2714">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2715">Az.Compute</span></span>
* <span data-ttu-id="37a30-2716">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="37a30-2717">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="37a30-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="37a30-2718">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="37a30-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2720">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="37a30-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="37a30-2721">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="37a30-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="37a30-2722">Az.Insights</span></span>
* <span data-ttu-id="37a30-2723">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="37a30-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="37a30-2724">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="37a30-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="37a30-2725">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="37a30-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="37a30-2726">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2727">Az.Network</span></span>
* <span data-ttu-id="37a30-2728">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37a30-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="37a30-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="37a30-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="37a30-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="37a30-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="37a30-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="37a30-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="37a30-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="37a30-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="37a30-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="37a30-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="37a30-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="37a30-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37a30-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37a30-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="37a30-2736">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2737">Az.Resources</span></span>
* <span data-ttu-id="37a30-2738">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="37a30-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="37a30-2739">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="37a30-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37a30-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37a30-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="37a30-2741">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="37a30-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37a30-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37a30-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="37a30-2743">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="37a30-2744">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="37a30-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="37a30-2745">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="37a30-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="37a30-2746">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="37a30-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="37a30-2747">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="37a30-2748">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="37a30-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37a30-2749">Az.Profile</span></span>
* <span data-ttu-id="37a30-2750">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="37a30-2751">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2752">Az.Compute</span></span>
* <span data-ttu-id="37a30-2753">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="37a30-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="37a30-2754">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37a30-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37a30-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="37a30-2756">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="37a30-2757">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="37a30-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="37a30-2758">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="37a30-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="37a30-2759">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="37a30-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="37a30-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="37a30-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2761">Az.Network</span></span>
* <span data-ttu-id="37a30-2762">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="37a30-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="37a30-2763">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2764">Az.Resources</span></span>
* <span data-ttu-id="37a30-2765">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="37a30-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="37a30-2766">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="37a30-2767">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="37a30-2768">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="37a30-2768">Azure.Storage</span></span>
* <span data-ttu-id="37a30-2769">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="37a30-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="37a30-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37a30-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="37a30-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="37a30-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="37a30-2772">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="37a30-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="37a30-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="37a30-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37a30-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37a30-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="37a30-2775">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37a30-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37a30-2776">Az.Compute</span></span>
* <span data-ttu-id="37a30-2777">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="37a30-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="37a30-2778">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="37a30-2779">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="37a30-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="37a30-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="37a30-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="37a30-2781">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37a30-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37a30-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37a30-2782">Az.Network</span></span>
* <span data-ttu-id="37a30-2783">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37a30-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="37a30-2784">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2784">new cmdlets added</span></span>
    - <span data-ttu-id="37a30-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37a30-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="37a30-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37a30-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="37a30-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37a30-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="37a30-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37a30-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="37a30-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="37a30-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="37a30-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="37a30-2791">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="37a30-2792">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="37a30-2793">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37a30-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37a30-2794">Az.RedisCache</span></span>
* <span data-ttu-id="37a30-2795">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="37a30-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="37a30-2796">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="37a30-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37a30-2797">Az.Resources</span></span>
* <span data-ttu-id="37a30-2798">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="37a30-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="37a30-2799">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="37a30-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="37a30-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37a30-2800">Az.Sql</span></span>
* <span data-ttu-id="37a30-2801">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="37a30-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37a30-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37a30-2802">Az.Websites</span></span>
* <span data-ttu-id="37a30-2803">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="37a30-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="37a30-2804">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="37a30-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="37a30-2805">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="37a30-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="37a30-2806">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="37a30-2806">Initial Release</span></span>
