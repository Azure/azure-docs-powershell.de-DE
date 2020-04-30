---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: de813e8a4e3629a6fee6e87a0208c1f0362a16ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2020
ms.locfileid: "82080197"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="97013-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="97013-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="97013-104">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="97013-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="97013-105">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="97013-105">Highlights since the last release</span></span>
* <span data-ttu-id="97013-106">Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="97013-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-107">Az.Accounts</span></span>
* <span data-ttu-id="97013-108">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="97013-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="97013-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-109">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-110">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="97013-111">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-112">Az.Cdn</span></span>
* <span data-ttu-id="97013-113">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-115">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="97013-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-116">Az.Compute</span></span>
* <span data-ttu-id="97013-117">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="97013-118">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="97013-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-119">Az.IotHub</span></span>
* <span data-ttu-id="97013-120">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="97013-121">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="97013-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="97013-122">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="97013-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="97013-123">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="97013-124">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="97013-125">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="97013-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="97013-126">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="97013-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="97013-127">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="97013-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="97013-128">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-128">New cmdlets are:</span></span>
    - <span data-ttu-id="97013-129">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="97013-130">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="97013-131">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="97013-132">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="97013-133">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-134">Az.KeyVault</span></span>
* <span data-ttu-id="97013-135">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="97013-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="97013-136">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="97013-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="97013-137">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="97013-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="97013-138">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="97013-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="97013-139">Az.Maintenance</span></span>
* <span data-ttu-id="97013-140">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-141">Az.Monitor</span></span>
* <span data-ttu-id="97013-142">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="97013-143">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="97013-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="97013-144">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="97013-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="97013-145">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="97013-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="97013-146">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="97013-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="97013-147">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="97013-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="97013-148">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="97013-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="97013-149">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="97013-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-150">Az.Network</span></span>
* <span data-ttu-id="97013-151">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="97013-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="97013-152">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="97013-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="97013-153">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="97013-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="97013-154">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="97013-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="97013-155">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="97013-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="97013-156">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="97013-157">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="97013-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="97013-158">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="97013-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="97013-159">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="97013-160">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="97013-161">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="97013-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="97013-162">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="97013-163">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="97013-164">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="97013-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="97013-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="97013-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="97013-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="97013-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-168">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="97013-169">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-171">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="97013-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-172">Az.Sql</span></span>
* <span data-ttu-id="97013-173">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="97013-174">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="97013-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-175">Az.Storage</span></span>
* <span data-ttu-id="97013-176">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="97013-177">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="97013-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="97013-178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="97013-179">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="97013-180">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="97013-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="97013-181">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="97013-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="97013-182">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="97013-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="97013-183">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="97013-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="97013-184">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="97013-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="97013-185">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="97013-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="97013-186">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="97013-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="97013-187">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="97013-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="97013-188">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="97013-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="97013-189">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="97013-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="97013-190">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-190">General</span></span>
* <span data-ttu-id="97013-191">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97013-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="97013-192">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="97013-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="97013-193">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="97013-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="97013-194">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="97013-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="97013-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="97013-195">Az.Billing</span></span>
  - <span data-ttu-id="97013-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-196">Az.Compute</span></span>
  - <span data-ttu-id="97013-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="97013-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="97013-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-198">Az.EventHub</span></span>
  - <span data-ttu-id="97013-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-199">Az.IotHub</span></span>
  - <span data-ttu-id="97013-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-200">Az.KeyVault</span></span>
  - <span data-ttu-id="97013-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-201">Az.Monitor</span></span>
  - <span data-ttu-id="97013-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-202">Az.Network</span></span>
  - <span data-ttu-id="97013-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-203">Az.Resources</span></span>
  - <span data-ttu-id="97013-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-204">Az.Storage</span></span>
  - <span data-ttu-id="97013-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-205">Az.Websites</span></span>
* <span data-ttu-id="97013-206">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="97013-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="97013-207">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="97013-208">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="97013-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="97013-209">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="97013-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-210">Az.Accounts</span></span>
* <span data-ttu-id="97013-211">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="97013-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-212">Az.Compute</span></span>
* <span data-ttu-id="97013-213">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="97013-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="97013-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="97013-215">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="97013-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="97013-216">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="97013-217">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="97013-217">[#11354]</span></span>
* <span data-ttu-id="97013-218">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="97013-219">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="97013-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="97013-220">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="97013-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="97013-221">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="97013-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="97013-222">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="97013-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="97013-223">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="97013-224">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="97013-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="97013-225">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="97013-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="97013-226">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="97013-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-227">Az.DataFactory</span></span>
* <span data-ttu-id="97013-228">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="97013-229">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-231">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="97013-232">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="97013-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-233">Az.HDInsight</span></span>
* <span data-ttu-id="97013-234">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="97013-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-235">Az.IotHub</span></span>
* <span data-ttu-id="97013-236">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="97013-237">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="97013-238">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="97013-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="97013-239">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="97013-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-240">Az.KeyVault</span></span>
* <span data-ttu-id="97013-241">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-242">Az.Monitor</span></span>
* <span data-ttu-id="97013-243">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-244">Az.Network</span></span>
* <span data-ttu-id="97013-245">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="97013-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="97013-246">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="97013-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="97013-247">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="97013-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="97013-248">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="97013-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="97013-249">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="97013-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="97013-250">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-252">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="97013-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-254">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="97013-255">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="97013-256">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="97013-257">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="97013-258">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="97013-259">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-260">Az.Resources</span></span>
* <span data-ttu-id="97013-261">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="97013-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="97013-262">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="97013-263">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="97013-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="97013-264">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-264">Added example.</span></span>
* <span data-ttu-id="97013-265">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="97013-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="97013-266">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-267">Az.Sql</span></span>
* <span data-ttu-id="97013-268">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="97013-269">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="97013-270">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="97013-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="97013-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="97013-271">Az.Support</span></span>
* <span data-ttu-id="97013-272">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="97013-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-273">Az.Websites</span></span>
* <span data-ttu-id="97013-274">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="97013-275">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="97013-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="97013-276">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="97013-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="97013-277">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="97013-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="97013-278">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="97013-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="97013-279">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="97013-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-280">Az.Accounts</span></span>
* <span data-ttu-id="97013-281">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="97013-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="97013-282">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="97013-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="97013-283">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="97013-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-284">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-285">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="97013-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="97013-286">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="97013-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="97013-287">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="97013-288">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="97013-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-290">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-291">Az.IotHub</span></span>
* <span data-ttu-id="97013-292">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="97013-293">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="97013-294">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="97013-295">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="97013-296">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="97013-297">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="97013-298">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="97013-299">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="97013-300">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="97013-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="97013-301">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="97013-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="97013-302">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="97013-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="97013-303">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="97013-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="97013-304">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="97013-305">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="97013-306">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="97013-307">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="97013-308">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="97013-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="97013-309">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="97013-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="97013-310">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-311">Az.Monitor</span></span>
* <span data-ttu-id="97013-312">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="97013-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-313">Az.Network</span></span>
* <span data-ttu-id="97013-314">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97013-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="97013-315">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="97013-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="97013-316">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="97013-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="97013-317">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-318">Az.Resources</span></span>
* <span data-ttu-id="97013-319">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="97013-320">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="97013-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="97013-321">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="97013-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="97013-322">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="97013-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="97013-323">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="97013-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="97013-324">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="97013-325">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="97013-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="97013-326">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="97013-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="97013-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="97013-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="97013-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="97013-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="97013-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="97013-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="97013-330">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="97013-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="97013-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="97013-332">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="97013-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-333">Az.Sql</span></span>
* <span data-ttu-id="97013-334">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="97013-335">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="97013-336">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="97013-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="97013-337">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="97013-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="97013-338">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="97013-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="97013-339">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="97013-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="97013-340">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="97013-341">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="97013-342">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="97013-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-343">Az.Storage</span></span>
* <span data-ttu-id="97013-344">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="97013-345">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="97013-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="97013-346">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="97013-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="97013-347">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="97013-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="97013-348">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="97013-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-349">Az.Websites</span></span>
* <span data-ttu-id="97013-350">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="97013-351">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="97013-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="97013-352">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="97013-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="97013-353">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="97013-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="97013-354">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="97013-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="97013-355">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="97013-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="97013-356">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="97013-356">Highlights since the last major release</span></span>
* <span data-ttu-id="97013-357">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="97013-358">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="97013-359">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-360">Az.Accounts</span></span>
* <span data-ttu-id="97013-361">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-362">Az.Automation</span></span>
* <span data-ttu-id="97013-363">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-365">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="97013-366">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="97013-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-367">Az.Compute</span></span>
* <span data-ttu-id="97013-368">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="97013-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="97013-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-369">Az.FrontDoor</span></span>
* <span data-ttu-id="97013-370">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="97013-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-371">Az.IotHub</span></span>
* <span data-ttu-id="97013-372">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="97013-373">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="97013-374">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="97013-375">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="97013-376">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="97013-377">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="97013-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-378">Az.KeyVault</span></span>
* <span data-ttu-id="97013-379">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-380">Az.Monitor</span></span>
* <span data-ttu-id="97013-381">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="97013-382">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="97013-383">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="97013-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-384">Az.Network</span></span>
* <span data-ttu-id="97013-385">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="97013-386">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="97013-387">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="97013-388">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="97013-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="97013-389">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-389">No new cmdlets are added.</span></span> <span data-ttu-id="97013-390">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="97013-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-392">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-393">Az.Resources</span></span>
* <span data-ttu-id="97013-394">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="97013-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="97013-395">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="97013-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="97013-396">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="97013-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="97013-397">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="97013-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="97013-398">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="97013-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="97013-399">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="97013-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="97013-400">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="97013-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="97013-401">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="97013-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-402">Az.Sql</span></span>
* <span data-ttu-id="97013-403">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="97013-404">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="97013-405">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="97013-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="97013-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="97013-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="97013-407">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="97013-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="97013-408">Az.StorageSync</span></span>
* <span data-ttu-id="97013-409">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="97013-410">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="97013-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="97013-411">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="97013-411">Highlights since the last major release</span></span>
* <span data-ttu-id="97013-412">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="97013-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="97013-413">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-414">Az.Accounts</span></span>
* <span data-ttu-id="97013-415">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="97013-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="97013-416">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="97013-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="97013-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-417">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-418">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="97013-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="97013-419">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="97013-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="97013-420">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="97013-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="97013-421">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="97013-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-422">Az.Compute</span></span>
* <span data-ttu-id="97013-423">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="97013-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="97013-424">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="97013-425">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="97013-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="97013-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="97013-427">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-428">Az.DataFactory</span></span>
* <span data-ttu-id="97013-429">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="97013-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="97013-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="97013-431">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="97013-432">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="97013-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-433">Az.HDInsight</span></span>
* <span data-ttu-id="97013-434">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-435">Az.KeyVault</span></span>
* <span data-ttu-id="97013-436">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="97013-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-437">Az.Network</span></span>
* <span data-ttu-id="97013-438">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="97013-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="97013-439">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="97013-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="97013-440">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="97013-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="97013-441">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="97013-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="97013-442">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="97013-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="97013-443">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="97013-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="97013-444">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="97013-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="97013-445">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="97013-446">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-446">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="97013-448">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="97013-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="97013-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="97013-450">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-452">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="97013-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="97013-453">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="97013-454">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="97013-455">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-457">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="97013-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="97013-458">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-459">Az.Resources</span></span>
* <span data-ttu-id="97013-460">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="97013-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="97013-461">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-462">Az.Sql</span></span>
<span data-ttu-id="97013-463">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="97013-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-464">Az.Storage</span></span>
* <span data-ttu-id="97013-465">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="97013-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="97013-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="97013-467">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="97013-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="97013-468">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-469">Az.Websites</span></span>
* <span data-ttu-id="97013-470">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="97013-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="97013-471">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="97013-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="97013-472">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="97013-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-473">Az.Accounts</span></span>
* <span data-ttu-id="97013-474">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="97013-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-475">Az.Cdn</span></span>
* <span data-ttu-id="97013-476">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="97013-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-477">Az.Compute</span></span>
* <span data-ttu-id="97013-478">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="97013-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="97013-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="97013-480">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="97013-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="97013-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="97013-482">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="97013-483">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="97013-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="97013-484">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="97013-485">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="97013-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="97013-486">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="97013-487">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="97013-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="97013-488">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="97013-489">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="97013-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="97013-490">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="97013-491">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="97013-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="97013-492">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="97013-493">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="97013-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="97013-494">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="97013-495">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="97013-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="97013-496">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="97013-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="97013-497">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="97013-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="97013-498">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="97013-499">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="97013-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-500">Az.DataFactory</span></span>
* <span data-ttu-id="97013-501">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="97013-502">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="97013-503">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="97013-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="97013-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="97013-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="97013-505">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-506">Az.EventHub</span></span>
* <span data-ttu-id="97013-507">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="97013-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-508">Az.HDInsight</span></span>
* <span data-ttu-id="97013-509">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="97013-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="97013-510">Az.MachineLearning</span></span>
* <span data-ttu-id="97013-511">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="97013-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="97013-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="97013-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="97013-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="97013-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="97013-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="97013-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="97013-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="97013-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="97013-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="97013-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="97013-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="97013-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="97013-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="97013-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-519">Az.Network</span></span>
* <span data-ttu-id="97013-520">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="97013-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-522">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="97013-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="97013-523">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="97013-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="97013-524">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="97013-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="97013-525">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="97013-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-526">Az.Resources</span></span>
* <span data-ttu-id="97013-527">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-528">Az.Sql</span></span>
* <span data-ttu-id="97013-529">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="97013-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="97013-530">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="97013-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="97013-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="97013-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="97013-532">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-533">Az.Storage</span></span>
* <span data-ttu-id="97013-534">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="97013-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="97013-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="97013-536">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="97013-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="97013-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="97013-538">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="97013-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="97013-539">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-539">General</span></span>
* <span data-ttu-id="97013-540">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-541">Az.Accounts</span></span>
* <span data-ttu-id="97013-542">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="97013-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="97013-543">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="97013-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="97013-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="97013-544">Az.Batch</span></span>
* <span data-ttu-id="97013-545">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="97013-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-546">Az.DataFactory</span></span>
* <span data-ttu-id="97013-547">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="97013-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-548">Az.FrontDoor</span></span>
* <span data-ttu-id="97013-549">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="97013-550">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="97013-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="97013-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="97013-552">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="97013-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-553">Az.KeyVault</span></span>
* <span data-ttu-id="97013-554">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="97013-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="97013-555">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="97013-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="97013-556">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-557">Az.Monitor</span></span>
* <span data-ttu-id="97013-558">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="97013-559">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="97013-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="97013-560">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="97013-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-561">Az.Network</span></span>
* <span data-ttu-id="97013-562">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="97013-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-563">Az.Resources</span></span>
* <span data-ttu-id="97013-564">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="97013-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="97013-565">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="97013-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-566">Az.Sql</span></span>
* <span data-ttu-id="97013-567">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-568">Az.Storage</span></span>
* <span data-ttu-id="97013-569">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="97013-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="97013-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="97013-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="97013-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="97013-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="97013-572">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="97013-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="97013-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="97013-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="97013-574">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="97013-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="97013-575">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="97013-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="97013-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="97013-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="97013-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="97013-578">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="97013-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="97013-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="97013-580">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="97013-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="97013-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="97013-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="97013-582">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="97013-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="97013-583">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="97013-583">Highlights since the last major release</span></span>
* <span data-ttu-id="97013-584">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="97013-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="97013-585">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="97013-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-586">Az.Compute</span></span>
* <span data-ttu-id="97013-587">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="97013-587">VM Reapply feature</span></span>
    - <span data-ttu-id="97013-588">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="97013-589">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="97013-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="97013-590">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="97013-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="97013-591">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="97013-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="97013-592">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="97013-593">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="97013-594">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="97013-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="97013-595">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="97013-596">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="97013-597">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="97013-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="97013-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="97013-599">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="97013-600">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="97013-600">Get the Order</span></span>
* <span data-ttu-id="97013-601">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="97013-602">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="97013-602">Create new Order</span></span>
* <span data-ttu-id="97013-603">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="97013-604">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="97013-604">Remove the Order</span></span>
* <span data-ttu-id="97013-605">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="97013-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="97013-606">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="97013-606">Now creates Local Share</span></span>
* <span data-ttu-id="97013-607">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="97013-608">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="97013-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="97013-609">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="97013-610">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="97013-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="97013-611">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="97013-612">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="97013-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="97013-613">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="97013-614">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="97013-614">Create new Triggers</span></span>
* <span data-ttu-id="97013-615">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="97013-616">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="97013-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-617">Az.DataFactory</span></span>
* <span data-ttu-id="97013-618">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="97013-619">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="97013-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-621">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-622">Az.EventHub</span></span>
* <span data-ttu-id="97013-623">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="97013-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-624">Az.FrontDoor</span></span>
* <span data-ttu-id="97013-625">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="97013-626">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="97013-627">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="97013-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="97013-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-629">Az.Network</span></span>
* <span data-ttu-id="97013-630">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="97013-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="97013-631">Az.PrivateDns</span></span>
* <span data-ttu-id="97013-632">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-634">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="97013-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="97013-635">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="97013-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="97013-636">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="97013-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="97013-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="97013-637">Az.RedisCache</span></span>
* <span data-ttu-id="97013-638">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="97013-639">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="97013-640">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-641">Az.Resources</span></span>
- <span data-ttu-id="97013-642">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="97013-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="97013-643">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="97013-644">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="97013-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="97013-645">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="97013-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="97013-646">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="97013-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-647">Az.Sql</span></span>
* <span data-ttu-id="97013-648">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="97013-649">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="97013-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="97013-650">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="97013-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="97013-651">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-651">General</span></span>
* <span data-ttu-id="97013-652">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="97013-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-653">Az.Accounts</span></span>
* <span data-ttu-id="97013-654">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="97013-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="97013-655">Az.Advisor</span></span>
* <span data-ttu-id="97013-656">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="97013-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="97013-657">Az.Batch</span></span>
* <span data-ttu-id="97013-658">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="97013-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="97013-659">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="97013-660">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="97013-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="97013-661">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97013-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="97013-662">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="97013-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="97013-663">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="97013-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="97013-664">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="97013-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="97013-665">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="97013-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="97013-666">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="97013-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="97013-667">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="97013-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="97013-668">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="97013-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="97013-669">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="97013-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="97013-670">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="97013-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="97013-671">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="97013-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="97013-672">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="97013-673">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="97013-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="97013-674">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="97013-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="97013-675">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="97013-676">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="97013-677">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97013-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="97013-678">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="97013-679">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="97013-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="97013-680">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="97013-681">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="97013-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="97013-682">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="97013-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="97013-683">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97013-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="97013-684">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="97013-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="97013-685">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="97013-686">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="97013-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="97013-687">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="97013-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="97013-688">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="97013-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="97013-689">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="97013-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="97013-690">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="97013-691">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="97013-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="97013-692">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="97013-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="97013-693">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="97013-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-694">Az.Cdn</span></span>
* <span data-ttu-id="97013-695">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="97013-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="97013-696">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="97013-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-697">Az.Compute</span></span>
* <span data-ttu-id="97013-698">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="97013-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="97013-699">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="97013-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="97013-700">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="97013-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="97013-701">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="97013-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="97013-702">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="97013-703">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="97013-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="97013-704">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="97013-705">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="97013-705">Breaking changes</span></span>
    - <span data-ttu-id="97013-706">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="97013-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="97013-707">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="97013-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-708">Az.DataFactory</span></span>
* <span data-ttu-id="97013-709">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97013-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-711">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="97013-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="97013-712">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="97013-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="97013-713">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="97013-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="97013-714">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="97013-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="97013-715">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="97013-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="97013-716">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="97013-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="97013-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-717">Az.FrontDoor</span></span>
* <span data-ttu-id="97013-718">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="97013-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-719">Az.HDInsight</span></span>
* <span data-ttu-id="97013-720">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="97013-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="97013-721">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="97013-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="97013-722">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="97013-723">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="97013-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="97013-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="97013-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="97013-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="97013-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="97013-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="97013-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="97013-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="97013-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="97013-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="97013-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="97013-729">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="97013-730">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="97013-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="97013-731">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="97013-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="97013-732">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="97013-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="97013-733">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="97013-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="97013-734">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="97013-735">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="97013-736">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="97013-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="97013-737">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="97013-738">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="97013-739">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="97013-740">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="97013-741">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="97013-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-742">Az.IotHub</span></span>
* <span data-ttu-id="97013-743">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="97013-743">Breaking changes:</span></span>
    - <span data-ttu-id="97013-744">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="97013-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="97013-745">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="97013-746">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="97013-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="97013-747">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="97013-748">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="97013-749">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="97013-750">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="97013-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="97013-751">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="97013-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="97013-752">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="97013-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="97013-753">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="97013-754">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="97013-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="97013-755">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-757">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="97013-758">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="97013-759">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="97013-760">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="97013-761">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="97013-762">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="97013-763">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="97013-764">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="97013-765">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-766">Az.Resources</span></span>
* <span data-ttu-id="97013-767">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97013-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-768">Az.Network</span></span>
* <span data-ttu-id="97013-769">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="97013-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="97013-770">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="97013-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="97013-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="97013-776">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="97013-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="97013-777">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="97013-777">New cmdlet:</span></span>
        - <span data-ttu-id="97013-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="97013-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="97013-779">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="97013-780">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="97013-781">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="97013-782">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="97013-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="97013-783">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="97013-784">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="97013-785">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="97013-786">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-786">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="97013-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="97013-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="97013-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="97013-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="97013-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="97013-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="97013-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="97013-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="97013-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="97013-792">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="97013-793">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="97013-794">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="97013-795">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="97013-796">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="97013-797">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="97013-798">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="97013-799">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-799">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="97013-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="97013-801">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="97013-802">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="97013-803">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="97013-804">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="97013-805">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="97013-806">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="97013-807">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="97013-808">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-808">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="97013-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="97013-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="97013-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="97013-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="97013-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="97013-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="97013-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="97013-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="97013-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="97013-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="97013-815">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="97013-816">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="97013-817">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="97013-818">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="97013-819">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="97013-820">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="97013-821">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="97013-822">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="97013-823">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="97013-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="97013-824">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="97013-825">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="97013-826">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-826">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="97013-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="97013-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="97013-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="97013-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="97013-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="97013-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="97013-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-832">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="97013-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-833">Az.Sql</span></span>
* <span data-ttu-id="97013-834">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="97013-835">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="97013-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="97013-836">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="97013-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="97013-837">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="97013-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="97013-838">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="97013-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="97013-839">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="97013-840">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="97013-841">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="97013-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="97013-842">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-843">Az.Storage</span></span>
* <span data-ttu-id="97013-844">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="97013-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="97013-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="97013-847">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="97013-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="97013-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="97013-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="97013-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="97013-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="97013-850">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="97013-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="97013-851">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-851">General</span></span>
* <span data-ttu-id="97013-852">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="97013-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-853">Az.Accounts</span></span>
* <span data-ttu-id="97013-854">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="97013-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-855">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-856">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="97013-857">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="97013-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-858">Az.Automation</span></span>
* <span data-ttu-id="97013-859">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="97013-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="97013-860">Az.Batch</span></span>
* <span data-ttu-id="97013-861">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="97013-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-862">Az.Compute</span></span>
* <span data-ttu-id="97013-863">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="97013-864">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="97013-865">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="97013-866">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="97013-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-867">Az.DataFactory</span></span>
* <span data-ttu-id="97013-868">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="97013-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="97013-869">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="97013-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="97013-870">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-872">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="97013-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="97013-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="97013-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="97013-874">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="97013-875">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="97013-876">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="97013-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="97013-877">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="97013-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-878">Az.IotHub</span></span>
* <span data-ttu-id="97013-879">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="97013-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="97013-880">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="97013-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-881">Az.Monitor</span></span>
* <span data-ttu-id="97013-882">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="97013-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="97013-883">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="97013-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="97013-884">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="97013-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="97013-885">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="97013-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-886">Az.Network</span></span>
* <span data-ttu-id="97013-887">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="97013-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="97013-888">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="97013-889">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-889">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="97013-891">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="97013-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="97013-892">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="97013-893">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="97013-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="97013-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="97013-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="97013-897">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="97013-898">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="97013-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="97013-899">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="97013-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="97013-900">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="97013-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="97013-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="97013-901">Az.RedisCache</span></span>
* <span data-ttu-id="97013-902">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="97013-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-903">Az.Sql</span></span>
* <span data-ttu-id="97013-904">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-905">Az.Storage</span></span>
* <span data-ttu-id="97013-906">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="97013-907">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="97013-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="97013-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97013-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="97013-909">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="97013-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="97013-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="97013-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="97013-911">Az.StorageSync</span></span>
* <span data-ttu-id="97013-912">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-913">Az.Websites</span></span>
* <span data-ttu-id="97013-914">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="97013-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="97013-915">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="97013-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="97013-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-916">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-917">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="97013-918">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="97013-919">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="97013-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-920">Az.Automation</span></span>
* <span data-ttu-id="97013-921">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="97013-922">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="97013-923">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-924">Az.Compute</span></span>
* <span data-ttu-id="97013-925">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="97013-926">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="97013-927">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="97013-928">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="97013-929">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="97013-930">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="97013-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="97013-931">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="97013-932">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="97013-933">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-934">Az.DataFactory</span></span>
* <span data-ttu-id="97013-935">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="97013-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="97013-936">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="97013-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-937">Az.HDInsight</span></span>
* <span data-ttu-id="97013-938">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-939">Az.IotHub</span></span>
* <span data-ttu-id="97013-940">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="97013-941">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="97013-942">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="97013-942">New cmdlets are:</span></span>
    - <span data-ttu-id="97013-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="97013-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="97013-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="97013-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="97013-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="97013-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="97013-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="97013-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-947">Az.Monitor</span></span>
* <span data-ttu-id="97013-948">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="97013-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="97013-949">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="97013-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="97013-950">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="97013-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="97013-951">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="97013-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="97013-952">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="97013-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="97013-953">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="97013-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="97013-954">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="97013-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="97013-955">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="97013-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="97013-956">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="97013-957">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="97013-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="97013-958">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="97013-959">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="97013-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="97013-960">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="97013-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="97013-961">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="97013-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="97013-962">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="97013-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="97013-963">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="97013-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="97013-964">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="97013-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="97013-965">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="97013-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="97013-966">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="97013-967">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="97013-967">Overall improved help files</span></span>
* <span data-ttu-id="97013-968">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-969">Az.Network</span></span>
* <span data-ttu-id="97013-970">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="97013-971">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="97013-972">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="97013-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="97013-973">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="97013-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="97013-974">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="97013-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="97013-975">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="97013-976">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="97013-977">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="97013-978">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="97013-979">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="97013-980">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="97013-981">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="97013-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="97013-982">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-982">New cmdlets</span></span>
        - <span data-ttu-id="97013-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="97013-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="97013-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="97013-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="97013-985">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="97013-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="97013-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="97013-986">New-VpnSite</span></span>
        - <span data-ttu-id="97013-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="97013-987">Update-VpnSite</span></span>
        - <span data-ttu-id="97013-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="97013-988">New-VpnConnection</span></span>
        - <span data-ttu-id="97013-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="97013-989">Update-VpnConnection</span></span>
* <span data-ttu-id="97013-990">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="97013-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-992">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="97013-993">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-994">Az.Resources</span></span>
* <span data-ttu-id="97013-995">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="97013-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-997">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="97013-998">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="97013-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="97013-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="97013-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="97013-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="97013-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="97013-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="97013-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="97013-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="97013-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="97013-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="97013-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="97013-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="97013-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="97013-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="97013-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="97013-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="97013-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="97013-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="97013-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="97013-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="97013-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="97013-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="97013-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="97013-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="97013-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="97013-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="97013-1012">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="97013-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="97013-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="97013-1013">Az.SignalR</span></span>
* <span data-ttu-id="97013-1014">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1015">Az.Sql</span></span>
* <span data-ttu-id="97013-1016">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="97013-1017">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="97013-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="97013-1018">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="97013-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="97013-1019">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="97013-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="97013-1020">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="97013-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1021">Az.Storage</span></span>
* <span data-ttu-id="97013-1022">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="97013-1023">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97013-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="97013-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="97013-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="97013-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="97013-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="97013-1026">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="97013-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="97013-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="97013-1028">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="97013-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="97013-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="97013-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="97013-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="97013-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="97013-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="97013-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="97013-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="97013-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1033">Az.Websites</span></span>
* <span data-ttu-id="97013-1034">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="97013-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="97013-1035">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="97013-1036">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="97013-1037">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="97013-1038">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-1038">General</span></span>
* <span data-ttu-id="97013-1039">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1040">Az.Accounts</span></span>
* <span data-ttu-id="97013-1041">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="97013-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="97013-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="97013-1042">Az.Aks</span></span>
* <span data-ttu-id="97013-1043">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="97013-1044">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="97013-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="97013-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-1046">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="97013-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="97013-1047">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="97013-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="97013-1048">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="97013-1049">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="97013-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="97013-1050">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="97013-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="97013-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="97013-1051">Az.Batch</span></span>
* <span data-ttu-id="97013-1052">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="97013-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-1053">Az.Cdn</span></span>
* <span data-ttu-id="97013-1054">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1055">Az.Compute</span></span>
* <span data-ttu-id="97013-1056">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="97013-1057">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="97013-1058">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="97013-1059">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="97013-1060">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="97013-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="97013-1061">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="97013-1062">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="97013-1063">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1064">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1065">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="97013-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="97013-1066">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="97013-1067">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="97013-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="97013-1068">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-1070">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-1071">Az.EventHub</span></span>
* <span data-ttu-id="97013-1072">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="97013-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="97013-1073">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="97013-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="97013-1074">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="97013-1075">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="97013-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="97013-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="97013-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="97013-1077">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-1078">Az.Monitor</span></span>
* <span data-ttu-id="97013-1079">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1080">Az.Network</span></span>
* <span data-ttu-id="97013-1081">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="97013-1082">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="97013-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="97013-1083">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="97013-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="97013-1084">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="97013-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="97013-1085">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="97013-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="97013-1086">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="97013-1087">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="97013-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="97013-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="97013-1089">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="97013-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="97013-1090">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1090">Added example</span></span>
    - <span data-ttu-id="97013-1091">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="97013-1092">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="97013-1093">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="97013-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1095">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1096">Az.Resources</span></span>
* <span data-ttu-id="97013-1097">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="97013-1098">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="97013-1099">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="97013-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="97013-1100">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="97013-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="97013-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="97013-1102">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="97013-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="97013-1103">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="97013-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="97013-1104">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-1106">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="97013-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="97013-1107">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="97013-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="97013-1108">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="97013-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="97013-1109">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="97013-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="97013-1110">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="97013-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="97013-1111">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="97013-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1112">Az.Sql</span></span>
* <span data-ttu-id="97013-1113">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1114">Az.Storage</span></span>
* <span data-ttu-id="97013-1115">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="97013-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="97013-1116">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="97013-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="97013-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="97013-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="97013-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="97013-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="97013-1119">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="97013-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="97013-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="97013-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1121">Az.Websites</span></span>
* <span data-ttu-id="97013-1122">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="97013-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="97013-1123">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1124">Az.Accounts</span></span>
* <span data-ttu-id="97013-1125">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="97013-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="97013-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="97013-1127">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1128">Az.Automation</span></span>
* <span data-ttu-id="97013-1129">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-1131">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1132">Az.Compute</span></span>
* <span data-ttu-id="97013-1133">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="97013-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97013-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="97013-1135">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="97013-1136">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="97013-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1137">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1138">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="97013-1139">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-1140">Az.EventHub</span></span>
* <span data-ttu-id="97013-1141">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="97013-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="97013-1142">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="97013-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-1143">Az.KeyVault</span></span>
* <span data-ttu-id="97013-1144">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="97013-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="97013-1145">Az.LogicApp</span></span>
* <span data-ttu-id="97013-1146">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="97013-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="97013-1147">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="97013-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="97013-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="97013-1149">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1150">Az.Network</span></span>
* <span data-ttu-id="97013-1151">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="97013-1152">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1152">New cmdlets</span></span>
        - <span data-ttu-id="97013-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="97013-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="97013-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97013-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="97013-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="97013-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="97013-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="97013-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97013-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="97013-1161">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97013-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="97013-1162">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="97013-1163">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="97013-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="97013-1164">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="97013-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="97013-1165">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="97013-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="97013-1166">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="97013-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="97013-1167">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="97013-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="97013-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="97013-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="97013-1171">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="97013-1172">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="97013-1173">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="97013-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="97013-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="97013-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="97013-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="97013-1177">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="97013-1178">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97013-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="97013-1179">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="97013-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="97013-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="97013-1181">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="97013-1182">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1184">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="97013-1185">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="97013-1186">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="97013-1187">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="97013-1188">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="97013-1189">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="97013-1190">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="97013-1191">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="97013-1192">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="97013-1193">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1194">Az.Resources</span></span>
- <span data-ttu-id="97013-1195">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="97013-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="97013-1196">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="97013-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="97013-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="97013-1198">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="97013-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="97013-1199">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="97013-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1200">Az.Sql</span></span>
* <span data-ttu-id="97013-1201">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="97013-1202">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="97013-1203">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1204">Az.Storage</span></span>
* <span data-ttu-id="97013-1205">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="97013-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="97013-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="97013-1206">Az.StorageSync</span></span>
* <span data-ttu-id="97013-1207">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="97013-1208">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1209">Az.Websites</span></span>
* <span data-ttu-id="97013-1210">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="97013-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="97013-1211">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="97013-1212">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="97013-1213">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1214">Az.Accounts</span></span>
* <span data-ttu-id="97013-1215">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="97013-1216">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="97013-1217">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="97013-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="97013-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="97013-1218">Az.Advisor</span></span>
* <span data-ttu-id="97013-1219">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="97013-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="97013-1220">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="97013-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="97013-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-1222">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="97013-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="97013-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="97013-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="97013-1224">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="97013-1225">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="97013-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="97013-1226">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="97013-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="97013-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="97013-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="97013-1228">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1229">Az.Automation</span></span>
* <span data-ttu-id="97013-1230">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1231">Az.Compute</span></span>
* <span data-ttu-id="97013-1232">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1233">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1234">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="97013-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="97013-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="97013-1235">Az.EventGrid</span></span>
* <span data-ttu-id="97013-1236">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-1237">Az.IotHub</span></span>
* <span data-ttu-id="97013-1238">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1239">Az.Network</span></span>
* <span data-ttu-id="97013-1240">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="97013-1241">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="97013-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-1243">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="97013-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="97013-1244">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="97013-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="97013-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="97013-1246">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1248">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="97013-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1249">Az.Resources</span></span>
    - <span data-ttu-id="97013-1250">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="97013-1251">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="97013-1252">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="97013-1253">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="97013-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="97013-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="97013-1255">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="97013-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1256">Az.Sql</span></span>
* <span data-ttu-id="97013-1257">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="97013-1258">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="97013-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="97013-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="97013-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="97013-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="97013-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="97013-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="97013-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="97013-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="97013-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="97013-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="97013-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="97013-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="97013-1265">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1266">Az.Storage</span></span>
* <span data-ttu-id="97013-1267">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="97013-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="97013-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="97013-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="97013-1269">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="97013-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="97013-1270">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="97013-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="97013-1271">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="97013-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="97013-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="97013-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="97013-1274">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="97013-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="97013-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="97013-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="97013-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="97013-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="97013-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="97013-1277">Az.StorageSync</span></span>
* <span data-ttu-id="97013-1278">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="97013-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="97013-1279">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1280">Az.Accounts</span></span>
* <span data-ttu-id="97013-1281">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="97013-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="97013-1282">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="97013-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="97013-1283">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="97013-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="97013-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="97013-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="97013-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1286">Az.Compute</span></span>
* <span data-ttu-id="97013-1287">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="97013-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="97013-1288">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="97013-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="97013-1289">Az.Dns</span></span>
* <span data-ttu-id="97013-1290">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="97013-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="97013-1291">Az.EventGrid</span></span>
* <span data-ttu-id="97013-1292">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="97013-1293">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-1293">New cmdlets:</span></span>
    - <span data-ttu-id="97013-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="97013-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="97013-1295">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="97013-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="97013-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="97013-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="97013-1297">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="97013-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="97013-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="97013-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="97013-1299">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="97013-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="97013-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="97013-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="97013-1301">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="97013-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="97013-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="97013-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="97013-1303">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97013-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="97013-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="97013-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="97013-1305">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="97013-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="97013-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="97013-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="97013-1307">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="97013-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="97013-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="97013-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="97013-1309">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="97013-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="97013-1310">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="97013-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="97013-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="97013-1312">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="97013-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="97013-1313">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="97013-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="97013-1314">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="97013-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="97013-1315">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="97013-1316">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="97013-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="97013-1317">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="97013-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="97013-1318">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="97013-1319">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="97013-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="97013-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="97013-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="97013-1321">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="97013-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="97013-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="97013-1323">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="97013-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="97013-1324">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="97013-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="97013-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="97013-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="97013-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="97013-1327">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="97013-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="97013-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="97013-1329">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1330">Az.Network</span></span>
* <span data-ttu-id="97013-1331">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="97013-1332">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1332">New cmdlets</span></span>
        - <span data-ttu-id="97013-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="97013-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="97013-1334">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="97013-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="97013-1335">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1335">New cmdlets</span></span>
        - <span data-ttu-id="97013-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="97013-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="97013-1337">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="97013-1338">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1338">New cmdlets</span></span>
        - <span data-ttu-id="97013-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97013-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="97013-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97013-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="97013-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97013-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="97013-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="97013-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="97013-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="97013-1344">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="97013-1345">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1345">New cmdlets</span></span>
        - <span data-ttu-id="97013-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="97013-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="97013-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="97013-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="97013-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="97013-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="97013-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="97013-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="97013-1350">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="97013-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="97013-1351">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="97013-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="97013-1352">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="97013-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="97013-1353">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="97013-1354">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="97013-1355">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="97013-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="97013-1356">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="97013-1357">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="97013-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="97013-1358">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="97013-1359">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="97013-1360">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="97013-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="97013-1361">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="97013-1362">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="97013-1363">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="97013-1364">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="97013-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="97013-1365">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="97013-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="97013-1366">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="97013-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="97013-1367">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="97013-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="97013-1368">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="97013-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="97013-1369">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="97013-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="97013-1370">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="97013-1371">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="97013-1372">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="97013-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="97013-1374">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="97013-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1375">Az.Resources</span></span>
* <span data-ttu-id="97013-1376">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="97013-1377">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="97013-1378">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="97013-1379">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="97013-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-1381">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="97013-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1382">Az.Sql</span></span>
* <span data-ttu-id="97013-1383">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="97013-1384">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="97013-1385">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="97013-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="97013-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97013-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="97013-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97013-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="97013-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97013-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="97013-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="97013-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="97013-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="97013-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1391">Az.Storage</span></span>
* <span data-ttu-id="97013-1392">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="97013-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="97013-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="97013-1394">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="97013-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="97013-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1396">Az.Websites</span></span>
* <span data-ttu-id="97013-1397">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="97013-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="97013-1398">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="97013-1399">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="97013-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-1400">Az.Cdn</span></span>
* <span data-ttu-id="97013-1401">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="97013-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1402">Az.Compute</span></span>
* <span data-ttu-id="97013-1403">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="97013-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="97013-1404">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="97013-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-1405">Az.EventHub</span></span>
* <span data-ttu-id="97013-1406">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="97013-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="97013-1407">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="97013-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1408">Az.Network</span></span>
* <span data-ttu-id="97013-1409">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="97013-1410">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-1412">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="97013-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1414">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="97013-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="97013-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="97013-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="97013-1416">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="97013-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-1418">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="97013-1419">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1420">Az.Sql</span></span>
* <span data-ttu-id="97013-1421">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="97013-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="97013-1422">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="97013-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="97013-1423">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="97013-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="97013-1424">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="97013-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1425">Az.Websites</span></span>
* <span data-ttu-id="97013-1426">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="97013-1427">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="97013-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-1429">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="97013-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="97013-1430">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="97013-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="97013-1431">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="97013-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="97013-1432">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="97013-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="97013-1433">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="97013-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="97013-1434">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="97013-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="97013-1435">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="97013-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="97013-1436">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="97013-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="97013-1437">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="97013-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="97013-1438">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="97013-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="97013-1439">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="97013-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="97013-1440">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="97013-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="97013-1441">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="97013-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="97013-1442">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="97013-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="97013-1443">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="97013-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="97013-1444">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="97013-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="97013-1445">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="97013-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="97013-1446">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="97013-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="97013-1447">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="97013-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="97013-1448">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="97013-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="97013-1449">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="97013-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="97013-1450">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="97013-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="97013-1451">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="97013-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="97013-1452">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="97013-1453">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="97013-1454">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="97013-1455">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="97013-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="97013-1456">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="97013-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="97013-1457">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="97013-1458">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="97013-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="97013-1459">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="97013-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="97013-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="97013-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="97013-1461">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="97013-1462">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="97013-1463">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="97013-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="97013-1464">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="97013-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="97013-1465">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="97013-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="97013-1466">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="97013-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="97013-1467">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="97013-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="97013-1468">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="97013-1469">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="97013-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="97013-1470">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="97013-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="97013-1471">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="97013-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="97013-1472">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="97013-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="97013-1473">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="97013-1474">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="97013-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="97013-1475">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="97013-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="97013-1476">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="97013-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="97013-1477">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="97013-1478">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="97013-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="97013-1479">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="97013-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="97013-1480">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="97013-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="97013-1481">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="97013-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="97013-1482">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="97013-1483">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="97013-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="97013-1484">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="97013-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="97013-1485">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="97013-1486">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="97013-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="97013-1487">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="97013-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="97013-1488">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="97013-1489">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="97013-1490">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="97013-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="97013-1491">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="97013-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="97013-1492">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="97013-1493">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="97013-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="97013-1494">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="97013-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="97013-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="97013-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="97013-1496">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="97013-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="97013-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="97013-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="97013-1498">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="97013-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="97013-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="97013-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="97013-1500">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="97013-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="97013-1501">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="97013-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="97013-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="97013-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="97013-1503">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="97013-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="97013-1504">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="97013-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="97013-1505">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="97013-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1506">Az.Automation</span></span>
* <span data-ttu-id="97013-1507">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="97013-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="97013-1508">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="97013-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="97013-1509">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="97013-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="97013-1510">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="97013-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="97013-1511">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="97013-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="97013-1512">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="97013-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="97013-1513">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="97013-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1514">Az.Compute</span></span>
* <span data-ttu-id="97013-1515">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="97013-1516">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="97013-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-1518">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="97013-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-1519">Az.Monitor</span></span>
* <span data-ttu-id="97013-1520">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="97013-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1521">Az.Network</span></span>
* <span data-ttu-id="97013-1522">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="97013-1523">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="97013-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="97013-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="97013-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="97013-1525">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="97013-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1526">Az.Resources</span></span>
* <span data-ttu-id="97013-1527">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1528">Az.Sql</span></span>
* <span data-ttu-id="97013-1529">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="97013-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="97013-1530">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1531">Az.Accounts</span></span>
* <span data-ttu-id="97013-1532">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="97013-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-1534">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="97013-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="97013-1535">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="97013-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1536">Az.Compute</span></span>
* <span data-ttu-id="97013-1537">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="97013-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="97013-1538">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="97013-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="97013-1539">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="97013-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="97013-1540">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="97013-1541">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="97013-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="97013-1542">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="97013-1543">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="97013-1543">Breaking changes</span></span>
    - <span data-ttu-id="97013-1544">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="97013-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="97013-1545">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="97013-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="97013-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="97013-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="97013-1547">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="97013-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="97013-1548">Az.Dns</span></span>
* <span data-ttu-id="97013-1549">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="97013-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="97013-1550">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="97013-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="97013-1551">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="97013-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="97013-1553">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="97013-1554">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="97013-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="97013-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-1555">Az.HDInsight</span></span>
* <span data-ttu-id="97013-1556">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="97013-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="97013-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="97013-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="97013-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="97013-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="97013-1559">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="97013-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="97013-1560">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="97013-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="97013-1561">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="97013-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="97013-1562">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="97013-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-1563">Az.Monitor</span></span>
* <span data-ttu-id="97013-1564">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="97013-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="97013-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="97013-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="97013-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="97013-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="97013-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="97013-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="97013-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="97013-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="97013-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="97013-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="97013-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="97013-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="97013-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="97013-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="97013-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="97013-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="97013-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="97013-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="97013-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="97013-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="97013-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="97013-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="97013-1576">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="97013-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="97013-1577">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="97013-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1578">Az.Network</span></span>
* <span data-ttu-id="97013-1579">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="97013-1580">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1580">New cmdlets</span></span>
        - <span data-ttu-id="97013-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="97013-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="97013-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="97013-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="97013-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="97013-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="97013-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="97013-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="97013-1585">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="97013-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="97013-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="97013-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="97013-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="97013-1588">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="97013-1589">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="97013-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="97013-1590">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="97013-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-1592">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="97013-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="97013-1593">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="97013-1594">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="97013-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1596">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="97013-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="97013-1597">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="97013-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="97013-1598">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="97013-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="97013-1599">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="97013-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="97013-1600">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="97013-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="97013-1601">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="97013-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="97013-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="97013-1602">Az.Relay</span></span>
* <span data-ttu-id="97013-1603">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="97013-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="97013-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="97013-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="97013-1605">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1606">Az.Storage</span></span>
* <span data-ttu-id="97013-1607">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="97013-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="97013-1608">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="97013-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="97013-1609">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="97013-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="97013-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="97013-1611">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="97013-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="97013-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="97013-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="97013-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1615">Az.Websites</span></span>
* <span data-ttu-id="97013-1616">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="97013-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="97013-1617">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="97013-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="97013-1618">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="97013-1619">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="97013-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="97013-1620">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="97013-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="97013-1621">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="97013-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="97013-1622">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="97013-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="97013-1623">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="97013-1624">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="97013-1625">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="97013-1626">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1627">Az.Accounts</span></span>
* <span data-ttu-id="97013-1628">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="97013-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="97013-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="97013-1629">Az.Batch</span></span>
* <span data-ttu-id="97013-1630">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-1631">Az.Cdn</span></span>
* <span data-ttu-id="97013-1632">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-1634">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1635">Az.Compute</span></span>
* <span data-ttu-id="97013-1636">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="97013-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="97013-1637">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="97013-1638">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1639">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1640">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="97013-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-1642">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="97013-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="97013-1643">Az.EventGrid</span></span>
* <span data-ttu-id="97013-1644">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="97013-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-1645">Az.EventHub</span></span>
* <span data-ttu-id="97013-1646">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="97013-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="97013-1647">Az.HDInsight</span></span>
* <span data-ttu-id="97013-1648">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-1649">Az.IotHub</span></span>
* <span data-ttu-id="97013-1650">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-1651">Az.KeyVault</span></span>
* <span data-ttu-id="97013-1652">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="97013-1653">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="97013-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="97013-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="97013-1655">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="97013-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="97013-1656">Az.Media</span></span>
* <span data-ttu-id="97013-1657">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-1658">Az.Monitor</span></span>
  * <span data-ttu-id="97013-1659">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="97013-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="97013-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="97013-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="97013-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="97013-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="97013-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="97013-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="97013-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="97013-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="97013-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="97013-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="97013-1665">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1666">Az.Network</span></span>
* <span data-ttu-id="97013-1667">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="97013-1668">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="97013-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="97013-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="97013-1670">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="97013-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="97013-1672">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="97013-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="97013-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="97013-1674">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1676">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="97013-1677">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="97013-1678">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="97013-1679">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="97013-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="97013-1680">Az.RedisCache</span></span>
* <span data-ttu-id="97013-1681">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1682">Az.Resources</span></span>
* <span data-ttu-id="97013-1683">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1684">Az.Sql</span></span>
* <span data-ttu-id="97013-1685">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="97013-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="97013-1686">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="97013-1687">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="97013-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="97013-1688">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="97013-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="97013-1689">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="97013-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="97013-1690">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="97013-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="97013-1691">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1692">Az.Websites</span></span>
* <span data-ttu-id="97013-1693">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="97013-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="97013-1694">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97013-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="97013-1695">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="97013-1696">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="97013-1697">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="97013-1698">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="97013-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="97013-1699">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="97013-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="97013-1700">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="97013-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="97013-1701">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="97013-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="97013-1702">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="97013-1703">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="97013-1704">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="97013-1705">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="97013-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1706">Az.Accounts</span></span>
* <span data-ttu-id="97013-1707">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="97013-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="97013-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="97013-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="97013-1709">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="97013-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="97013-1710">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="97013-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1711">Az.Automation</span></span>
* <span data-ttu-id="97013-1712">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="97013-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="97013-1713">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="97013-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="97013-1714">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="97013-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1715">Az.Compute</span></span>
* <span data-ttu-id="97013-1716">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="97013-1717">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="97013-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="97013-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="97013-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="97013-1719">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="97013-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1720">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1721">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="97013-1722">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1723">Az.Resources</span></span>
* <span data-ttu-id="97013-1724">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="97013-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="97013-1725">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="97013-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="97013-1726">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="97013-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="97013-1727">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="97013-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="97013-1728">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="97013-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="97013-1729">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="97013-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1730">Az.Sql</span></span>
* <span data-ttu-id="97013-1731">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="97013-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1732">Az.Storage</span></span>
* <span data-ttu-id="97013-1733">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="97013-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="97013-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="97013-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="97013-1735">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="97013-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="97013-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="97013-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="97013-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="97013-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="97013-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="97013-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="97013-1740">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="97013-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="97013-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="97013-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="97013-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="97013-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="97013-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="97013-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="97013-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="97013-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="97013-1745">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="97013-1746">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="97013-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="97013-1747">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="97013-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="97013-1748">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="97013-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="97013-1749">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="97013-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="97013-1750">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="97013-1751">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="97013-1752">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="97013-1753">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1754">Az.Automation</span></span>
* <span data-ttu-id="97013-1755">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="97013-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="97013-1756">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="97013-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="97013-1757">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="97013-1757">Pre-Post script</span></span>
    * <span data-ttu-id="97013-1758">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="97013-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1759">Az.Compute</span></span>
* <span data-ttu-id="97013-1760">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="97013-1761">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-1762">Az.KeyVault</span></span>
* <span data-ttu-id="97013-1763">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1764">Az.Network</span></span>
* <span data-ttu-id="97013-1765">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="97013-1766">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1768">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="97013-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="97013-1769">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1770">Az.Resources</span></span>
* <span data-ttu-id="97013-1771">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="97013-1772">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="97013-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1773">Az.Sql</span></span>
* <span data-ttu-id="97013-1774">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="97013-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1775">Az.Storage</span></span>
* <span data-ttu-id="97013-1776">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="97013-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="97013-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="97013-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="97013-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="97013-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="97013-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="97013-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="97013-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="97013-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="97013-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1783">Az.Websites</span></span>
* <span data-ttu-id="97013-1784">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="97013-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="97013-1785">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1786">Az.Accounts</span></span>
* <span data-ttu-id="97013-1787">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="97013-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="97013-1788">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97013-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1789">Az.Automation</span></span>
* <span data-ttu-id="97013-1790">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="97013-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="97013-1791">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="97013-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="97013-1792">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97013-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-1793">Az.Cdn</span></span>
* <span data-ttu-id="97013-1794">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="97013-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1795">Az.Compute</span></span>
* <span data-ttu-id="97013-1796">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1797">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1798">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="97013-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="97013-1799">Az.LogicApp</span></span>
* <span data-ttu-id="97013-1800">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="97013-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1801">Az.Network</span></span>
* <span data-ttu-id="97013-1802">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1804">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="97013-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="97013-1805">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="97013-1805">SDK Update</span></span>
* <span data-ttu-id="97013-1806">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="97013-1807">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1808">Az.Resources</span></span>
* <span data-ttu-id="97013-1809">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="97013-1810">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="97013-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="97013-1811">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="97013-1812">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="97013-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="97013-1813">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="97013-1814">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="97013-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1815">Az.Sql</span></span>
* <span data-ttu-id="97013-1816">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97013-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="97013-1817">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1818">Az.Storage</span></span>
* <span data-ttu-id="97013-1819">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97013-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="97013-1820">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="97013-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="97013-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="97013-1822">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="97013-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1823">Az.Automation</span></span>
* <span data-ttu-id="97013-1824">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="97013-1825">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="97013-1826">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="97013-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-1828">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97013-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1829">Az.Compute</span></span>
* <span data-ttu-id="97013-1830">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="97013-1831">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="97013-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="97013-1832">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="97013-1833">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="97013-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-1835">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="97013-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="97013-1836">Az.EventHub</span></span>
* <span data-ttu-id="97013-1837">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-1838">Az.KeyVault</span></span>
* <span data-ttu-id="97013-1839">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="97013-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="97013-1840">Az.LogicApp</span></span>
* <span data-ttu-id="97013-1841">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="97013-1842">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="97013-1843">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="97013-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="97013-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="97013-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="97013-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="97013-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="97013-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="97013-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="97013-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="97013-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="97013-1848">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="97013-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="97013-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="97013-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="97013-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="97013-1853">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="97013-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-1854">Az.Monitor</span></span>
* <span data-ttu-id="97013-1855">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1856">Az.Network</span></span>
* <span data-ttu-id="97013-1857">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="97013-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="97013-1859">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="97013-1860">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="97013-1861">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="97013-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1862">Az.Resources</span></span>
* <span data-ttu-id="97013-1863">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="97013-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="97013-1864">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="97013-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="97013-1865">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="97013-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="97013-1866">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="97013-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1867">Az.Sql</span></span>
* <span data-ttu-id="97013-1868">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="97013-1869">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="97013-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1870">Az.Websites</span></span>
* <span data-ttu-id="97013-1871">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="97013-1872">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1873">Az.Accounts</span></span>
* <span data-ttu-id="97013-1874">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="97013-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="97013-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="97013-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="97013-1876">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="97013-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1877">Az.Compute</span></span>
* <span data-ttu-id="97013-1878">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="97013-1879">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="97013-1880">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="97013-1882">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="97013-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1883">Az.Resources</span></span>
* <span data-ttu-id="97013-1884">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="97013-1885">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="97013-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="97013-1886">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="97013-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="97013-1887">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="97013-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1888">Az.Sql</span></span>
* <span data-ttu-id="97013-1889">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="97013-1890">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="97013-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="97013-1891">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="97013-1892">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1893">Az.Accounts</span></span>
* <span data-ttu-id="97013-1894">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="97013-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="97013-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="97013-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="97013-1896">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="97013-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="97013-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="97013-1898">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="97013-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="97013-1899">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1900">Az.Accounts</span></span>
* <span data-ttu-id="97013-1901">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="97013-1902">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="97013-1903">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="97013-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="97013-1904">Az.Aks</span></span>
* <span data-ttu-id="97013-1905">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="97013-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-1906">Az.Automation</span></span>
* <span data-ttu-id="97013-1907">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="97013-1908">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="97013-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="97013-1909">Az.Cdn</span></span>
* <span data-ttu-id="97013-1910">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1911">Az.Compute</span></span>
* <span data-ttu-id="97013-1912">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="97013-1913">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="97013-1914">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="97013-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97013-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="97013-1916">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="97013-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="97013-1917">Az.DataFactory</span></span>
* <span data-ttu-id="97013-1918">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-1920">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="97013-1921">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="97013-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="97013-1922">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-1923">Az.IotHub</span></span>
* <span data-ttu-id="97013-1924">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="97013-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-1925">Az.KeyVault</span></span>
* <span data-ttu-id="97013-1926">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-1927">Az.Network</span></span>
* <span data-ttu-id="97013-1928">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1929">Az.Resources</span></span>
* <span data-ttu-id="97013-1930">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="97013-1931">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="97013-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="97013-1932">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="97013-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="97013-1933">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="97013-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="97013-1934">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="97013-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="97013-1935">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="97013-1936">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="97013-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-1938">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="97013-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="97013-1939">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-1939">Fix some error messages.</span></span>
* <span data-ttu-id="97013-1940">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="97013-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="97013-1941">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="97013-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="97013-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="97013-1942">Az.SignalR</span></span>
* <span data-ttu-id="97013-1943">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1944">Az.Sql</span></span>
* <span data-ttu-id="97013-1945">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="97013-1946">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="97013-1947">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="97013-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="97013-1948">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="97013-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1949">Az.Storage</span></span>
* <span data-ttu-id="97013-1950">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="97013-1951">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="97013-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="97013-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="97013-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="97013-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="97013-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="97013-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="97013-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="97013-1955">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-1956">Az.Websites</span></span>
* <span data-ttu-id="97013-1957">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="97013-1958">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="97013-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="97013-1959">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="97013-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="97013-1960">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="97013-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="97013-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-1961">Az.Accounts</span></span>
* <span data-ttu-id="97013-1962">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-1963">Az.Compute</span></span>
* <span data-ttu-id="97013-1964">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="97013-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="97013-1965">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="97013-1966">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-1968">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="97013-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="97013-1969">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="97013-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="97013-1970">Az.EventGrid</span></span>
* <span data-ttu-id="97013-1971">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="97013-1972">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="97013-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="97013-1973">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="97013-1974">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="97013-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="97013-1975">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="97013-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="97013-1976">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="97013-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="97013-1977">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="97013-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="97013-1978">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="97013-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="97013-1979">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="97013-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="97013-1980">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="97013-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="97013-1981">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="97013-1982">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="97013-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="97013-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="97013-1983">Az.IotHub</span></span>
* <span data-ttu-id="97013-1984">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="97013-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="97013-1985">Az.LogicApp</span></span>
* <span data-ttu-id="97013-1986">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="97013-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-1987">Az.Resources</span></span>
* <span data-ttu-id="97013-1988">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="97013-1989">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="97013-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="97013-1990">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="97013-1991">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="97013-1992">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="97013-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="97013-1993">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="97013-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="97013-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="97013-1994">Az.SignalR</span></span>
* <span data-ttu-id="97013-1995">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="97013-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-1996">Az.Sql</span></span>
* <span data-ttu-id="97013-1997">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="97013-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="97013-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-1998">Az.Storage</span></span>
* <span data-ttu-id="97013-1999">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="97013-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="97013-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="97013-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="97013-2001">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="97013-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="97013-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="97013-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-2003">Az.Websites</span></span>
* <span data-ttu-id="97013-2004">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="97013-2005">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="97013-2006">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="97013-2007">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-2007">General</span></span>

- <span data-ttu-id="97013-2008">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="97013-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="97013-2009">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="97013-2009">Online help for each module</span></span>
- <span data-ttu-id="97013-2010">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="97013-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="97013-2011">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="97013-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="97013-2012">Az.Accounts</span></span>
- <span data-ttu-id="97013-2013">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="97013-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="97013-2014">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="97013-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="97013-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="97013-2016">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="97013-2016">Fixes for #7002</span></span>
- <span data-ttu-id="97013-2017">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="97013-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="97013-2018">Az.Batch</span></span>
- <span data-ttu-id="97013-2019">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="97013-2020">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="97013-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="97013-2021">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="97013-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="97013-2022">Az.Billing</span></span>
- <span data-ttu-id="97013-2023">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="97013-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="97013-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="97013-2025">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="97013-2026">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="97013-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="97013-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="97013-2028">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="97013-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="97013-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="97013-2030">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="97013-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="97013-2032">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="97013-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="97013-2033">Az.Monitor</span></span>
- <span data-ttu-id="97013-2034">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="97013-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="97013-2035">Az.KeyVault</span></span>
- <span data-ttu-id="97013-2036">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="97013-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="97013-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="97013-2038">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="97013-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="97013-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="97013-2039">Az.Media</span></span>
- <span data-ttu-id="97013-2040">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="97013-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="97013-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-2041">Az.Network</span></span>
<span data-ttu-id="97013-2042">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="97013-2043">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="97013-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="97013-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="97013-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="97013-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="97013-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97013-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="97013-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="97013-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="97013-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="97013-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="97013-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="97013-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="97013-2052">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="97013-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97013-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="97013-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97013-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="97013-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97013-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="97013-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97013-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="97013-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="97013-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="97013-2058">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="97013-2059">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="97013-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="97013-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97013-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="97013-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97013-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="97013-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97013-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="97013-2063">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="97013-2064">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="97013-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="97013-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="97013-2066">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="97013-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="97013-2067">Az.Profile</span></span>
- <span data-ttu-id="97013-2068">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="97013-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="97013-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="97013-2070">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="97013-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-2071">Az.Resources</span></span>
- <span data-ttu-id="97013-2072">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="97013-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="97013-2074">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="97013-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="97013-2075">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="97013-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="97013-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="97013-2077">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="97013-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="97013-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-2078">Az.Sql</span></span>
- <span data-ttu-id="97013-2079">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="97013-2080">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="97013-2081">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="97013-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-2082">Az.Storage</span></span>
- <span data-ttu-id="97013-2083">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="97013-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-2084">Az.Websites</span></span>
- <span data-ttu-id="97013-2085">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="97013-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="97013-2086">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="97013-2087">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-2087">General</span></span>

* <span data-ttu-id="97013-2088">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="97013-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="97013-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-2089">Az.Compute</span></span>

* <span data-ttu-id="97013-2090">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="97013-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="97013-2092">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="97013-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="97013-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="97013-2094">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="97013-2095">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="97013-2096">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="97013-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="97013-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="97013-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="97013-2098">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="97013-2099">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="97013-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="97013-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-2100">Az.Resources</span></span>

* <span data-ttu-id="97013-2101">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="97013-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="97013-2102">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="97013-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="97013-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-2103">Az.Sql</span></span>

* <span data-ttu-id="97013-2104">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="97013-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="97013-2105">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="97013-2106">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="97013-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="97013-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-2107">Az.Storage</span></span>

* <span data-ttu-id="97013-2108">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="97013-2109">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="97013-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="97013-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="97013-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="97013-2111">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="97013-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="97013-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="97013-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="97013-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="97013-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="97013-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-2114">Az.Websites</span></span>

* <span data-ttu-id="97013-2115">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="97013-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="97013-2116">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97013-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="97013-2117">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="97013-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="97013-2118">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="97013-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="97013-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="97013-2120">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="97013-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="97013-2121">Az.Automation</span></span>
* <span data-ttu-id="97013-2122">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="97013-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="97013-2123">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="97013-2124">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="97013-2125">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="97013-2126">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="97013-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-2127">Az.Compute</span></span>
* <span data-ttu-id="97013-2128">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="97013-2129">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="97013-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="97013-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="97013-2131">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="97013-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="97013-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="97013-2133">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="97013-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-2134">Az.Network</span></span>
* <span data-ttu-id="97013-2135">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="97013-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="97013-2136">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="97013-2137">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="97013-2138">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="97013-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="97013-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="97013-2140">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="97013-2141">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="97013-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="97013-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="97013-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="97013-2143">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="97013-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="97013-2144">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="97013-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="97013-2145">Az.Relay</span></span>
* <span data-ttu-id="97013-2146">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="97013-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="97013-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-2147">Az.Resources</span></span>
* <span data-ttu-id="97013-2148">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="97013-2149">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="97013-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="97013-2150">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="97013-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="97013-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-2152">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="97013-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-2153">Az.Sql</span></span>
* <span data-ttu-id="97013-2154">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="97013-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="97013-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="97013-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="97013-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="97013-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="97013-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="97013-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="97013-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="97013-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="97013-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="97013-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="97013-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="97013-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="97013-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="97013-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="97013-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="97013-2163">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="97013-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="97013-2164">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="97013-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="97013-2165">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="97013-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="97013-2166">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="97013-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="97013-2167">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="97013-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="97013-2168">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="97013-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="97013-2169">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="97013-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="97013-2170">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="97013-2171">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="97013-2172">Allgemein</span><span class="sxs-lookup"><span data-stu-id="97013-2172">General</span></span>
* <span data-ttu-id="97013-2173">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="97013-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="97013-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="97013-2174">Az.Profile</span></span>
* <span data-ttu-id="97013-2175">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="97013-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="97013-2176">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="97013-2177">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="97013-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="97013-2178">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="97013-2179">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="97013-2180">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="97013-2181">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="97013-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-2183">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-2184">Az.Compute</span></span>
* <span data-ttu-id="97013-2185">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="97013-2186">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="97013-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="97013-2187">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="97013-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-2189">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="97013-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="97013-2190">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="97013-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="97013-2191">Az.Insights</span></span>
* <span data-ttu-id="97013-2192">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="97013-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="97013-2193">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="97013-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="97013-2194">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="97013-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="97013-2195">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="97013-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-2196">Az.Network</span></span>
* <span data-ttu-id="97013-2197">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="97013-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="97013-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="97013-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="97013-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="97013-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="97013-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="97013-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="97013-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="97013-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="97013-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="97013-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="97013-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="97013-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="97013-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="97013-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="97013-2205">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-2206">Az.Resources</span></span>
* <span data-ttu-id="97013-2207">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="97013-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="97013-2208">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="97013-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="97013-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="97013-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="97013-2210">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="97013-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="97013-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="97013-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="97013-2212">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="97013-2213">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="97013-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="97013-2214">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="97013-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="97013-2215">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="97013-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="97013-2216">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="97013-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="97013-2217">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="97013-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="97013-2218">Az.Profile</span></span>
* <span data-ttu-id="97013-2219">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="97013-2220">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="97013-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-2221">Az.Compute</span></span>
* <span data-ttu-id="97013-2222">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="97013-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="97013-2223">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="97013-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97013-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="97013-2225">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="97013-2226">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="97013-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="97013-2227">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="97013-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="97013-2228">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="97013-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="97013-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="97013-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-2230">Az.Network</span></span>
* <span data-ttu-id="97013-2231">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="97013-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="97013-2232">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-2233">Az.Resources</span></span>
* <span data-ttu-id="97013-2234">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="97013-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="97013-2235">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97013-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="97013-2236">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="97013-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="97013-2237">Azure.Storage</span></span>
* <span data-ttu-id="97013-2238">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="97013-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="97013-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="97013-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="97013-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="97013-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="97013-2241">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="97013-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="97013-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="97013-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="97013-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="97013-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="97013-2244">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97013-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="97013-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="97013-2245">Az.Compute</span></span>
* <span data-ttu-id="97013-2246">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="97013-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="97013-2247">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="97013-2248">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="97013-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="97013-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="97013-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="97013-2250">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="97013-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="97013-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="97013-2251">Az.Network</span></span>
* <span data-ttu-id="97013-2252">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97013-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="97013-2253">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2253">new cmdlets added</span></span>
    - <span data-ttu-id="97013-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="97013-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="97013-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="97013-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="97013-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="97013-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="97013-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="97013-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="97013-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="97013-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="97013-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="97013-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="97013-2260">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="97013-2261">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="97013-2262">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="97013-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="97013-2263">Az.RedisCache</span></span>
* <span data-ttu-id="97013-2264">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="97013-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="97013-2265">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="97013-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="97013-2266">Az.Resources</span></span>
* <span data-ttu-id="97013-2267">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="97013-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="97013-2268">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="97013-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="97013-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="97013-2269">Az.Sql</span></span>
* <span data-ttu-id="97013-2270">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="97013-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="97013-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="97013-2271">Az.Websites</span></span>
* <span data-ttu-id="97013-2272">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="97013-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="97013-2273">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="97013-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="97013-2274">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="97013-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="97013-2275">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="97013-2275">Initial Release</span></span>
