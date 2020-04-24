---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740540"
---
## <a name="380---april-2020"></a><span data-ttu-id="a462c-103">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="a462c-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-104">Az.Accounts</span></span>
* <span data-ttu-id="a462c-105">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="a462c-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a462c-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-106">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-107">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a462c-108">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-109">Az.Cdn</span></span>
* <span data-ttu-id="a462c-110">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-112">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="a462c-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="a462c-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-113">Az.Compute</span></span>
* <span data-ttu-id="a462c-114">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="a462c-115">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="a462c-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-116">Az.IotHub</span></span>
* <span data-ttu-id="a462c-117">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a462c-118">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="a462c-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="a462c-119">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="a462c-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="a462c-120">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="a462c-121">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a462c-122">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a462c-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="a462c-123">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a462c-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="a462c-124">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="a462c-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="a462c-125">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-125">New cmdlets are:</span></span>
    - <span data-ttu-id="a462c-126">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a462c-127">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a462c-128">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a462c-129">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="a462c-130">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-131">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-132">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a462c-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="a462c-133">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="a462c-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="a462c-134">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="a462c-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="a462c-135">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a462c-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a462c-136">Az.Maintenance</span></span>
* <span data-ttu-id="a462c-137">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-138">Az.Monitor</span></span>
* <span data-ttu-id="a462c-139">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="a462c-140">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a462c-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a462c-141">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a462c-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a462c-142">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a462c-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a462c-143">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a462c-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a462c-144">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a462c-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a462c-145">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a462c-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a462c-146">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a462c-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-147">Az.Network</span></span>
* <span data-ttu-id="a462c-148">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a462c-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="a462c-149">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a462c-150">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a462c-151">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="a462c-152">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="a462c-153">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="a462c-154">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="a462c-155">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a462c-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="a462c-156">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="a462c-157">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a462c-158">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="a462c-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="a462c-159">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a462c-160">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="a462c-161">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a462c-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a462c-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="a462c-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-165">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="a462c-166">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-168">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a462c-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-169">Az.Sql</span></span>
* <span data-ttu-id="a462c-170">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="a462c-171">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="a462c-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-172">Az.Storage</span></span>
* <span data-ttu-id="a462c-173">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a462c-174">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="a462c-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="a462c-175">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a462c-176">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a462c-177">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="a462c-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="a462c-178">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a462c-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a462c-179">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a462c-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a462c-180">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="a462c-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="a462c-181">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a462c-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a462c-182">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="a462c-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="a462c-183">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a462c-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a462c-184">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="a462c-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="a462c-185">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a462c-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="a462c-186">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a462c-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="a462c-187">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="a462c-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-188">Az.Accounts</span></span>
* <span data-ttu-id="a462c-189">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="a462c-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-190">Az.Compute</span></span>
* <span data-ttu-id="a462c-191">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="a462c-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="a462c-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="a462c-193">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="a462c-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="a462c-194">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="a462c-195">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="a462c-195">[#11354]</span></span>
* <span data-ttu-id="a462c-196">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="a462c-197">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a462c-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a462c-198">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a462c-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a462c-199">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a462c-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a462c-200">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a462c-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="a462c-201">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="a462c-202">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a462c-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="a462c-203">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="a462c-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="a462c-204">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="a462c-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-205">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-206">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="a462c-207">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-209">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="a462c-210">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a462c-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-211">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-212">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="a462c-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-213">Az.IotHub</span></span>
* <span data-ttu-id="a462c-214">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="a462c-215">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="a462c-216">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a462c-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="a462c-217">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a462c-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-218">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-219">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-220">Az.Monitor</span></span>
* <span data-ttu-id="a462c-221">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-222">Az.Network</span></span>
* <span data-ttu-id="a462c-223">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="a462c-224">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a462c-225">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a462c-226">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a462c-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="a462c-227">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a462c-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="a462c-228">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-230">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="a462c-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-232">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="a462c-233">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="a462c-234">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="a462c-235">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="a462c-236">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="a462c-237">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-238">Az.Resources</span></span>
* <span data-ttu-id="a462c-239">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="a462c-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="a462c-240">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="a462c-241">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="a462c-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="a462c-242">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-242">Added example.</span></span>
* <span data-ttu-id="a462c-243">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="a462c-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="a462c-244">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-245">Az.Sql</span></span>
* <span data-ttu-id="a462c-246">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="a462c-247">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a462c-248">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="a462c-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="a462c-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="a462c-249">Az.Support</span></span>
* <span data-ttu-id="a462c-250">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="a462c-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-251">Az.Websites</span></span>
* <span data-ttu-id="a462c-252">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="a462c-253">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a462c-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a462c-254">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a462c-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a462c-255">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a462c-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a462c-256">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a462c-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="a462c-257">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="a462c-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-258">Az.Accounts</span></span>
* <span data-ttu-id="a462c-259">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="a462c-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="a462c-260">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="a462c-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="a462c-261">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a462c-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-262">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-263">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="a462c-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="a462c-264">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="a462c-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="a462c-265">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="a462c-266">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="a462c-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-268">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-269">Az.IotHub</span></span>
* <span data-ttu-id="a462c-270">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a462c-271">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="a462c-272">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a462c-273">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a462c-274">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a462c-275">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="a462c-276">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="a462c-277">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="a462c-278">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="a462c-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="a462c-279">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="a462c-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="a462c-280">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="a462c-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="a462c-281">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="a462c-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="a462c-282">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a462c-283">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a462c-284">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="a462c-285">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="a462c-286">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="a462c-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="a462c-287">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="a462c-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="a462c-288">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-289">Az.Monitor</span></span>
* <span data-ttu-id="a462c-290">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="a462c-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-291">Az.Network</span></span>
* <span data-ttu-id="a462c-292">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="a462c-293">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="a462c-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="a462c-294">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="a462c-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="a462c-295">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-296">Az.Resources</span></span>
* <span data-ttu-id="a462c-297">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="a462c-298">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="a462c-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="a462c-299">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="a462c-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="a462c-300">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="a462c-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="a462c-301">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="a462c-302">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="a462c-303">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="a462c-304">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="a462c-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="a462c-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a462c-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a462c-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a462c-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a462c-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a462c-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="a462c-308">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="a462c-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a462c-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="a462c-310">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="a462c-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-311">Az.Sql</span></span>
* <span data-ttu-id="a462c-312">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a462c-313">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="a462c-314">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="a462c-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="a462c-315">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="a462c-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="a462c-316">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="a462c-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="a462c-317">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="a462c-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="a462c-318">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="a462c-319">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="a462c-320">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="a462c-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-321">Az.Storage</span></span>
* <span data-ttu-id="a462c-322">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="a462c-323">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="a462c-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="a462c-324">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="a462c-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="a462c-325">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="a462c-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="a462c-326">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="a462c-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-327">Az.Websites</span></span>
* <span data-ttu-id="a462c-328">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="a462c-329">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="a462c-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="a462c-330">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="a462c-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="a462c-331">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="a462c-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="a462c-332">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="a462c-333">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="a462c-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a462c-334">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a462c-334">Highlights since the last major release</span></span>
* <span data-ttu-id="a462c-335">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="a462c-336">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="a462c-337">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-338">Az.Accounts</span></span>
* <span data-ttu-id="a462c-339">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-340">Az.Automation</span></span>
* <span data-ttu-id="a462c-341">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-343">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="a462c-344">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="a462c-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-345">Az.Compute</span></span>
* <span data-ttu-id="a462c-346">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="a462c-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a462c-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-347">Az.FrontDoor</span></span>
* <span data-ttu-id="a462c-348">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="a462c-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-349">Az.IotHub</span></span>
* <span data-ttu-id="a462c-350">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a462c-351">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="a462c-352">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a462c-353">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a462c-354">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a462c-355">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a462c-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-356">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-357">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-358">Az.Monitor</span></span>
* <span data-ttu-id="a462c-359">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="a462c-360">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="a462c-361">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="a462c-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-362">Az.Network</span></span>
* <span data-ttu-id="a462c-363">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="a462c-364">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a462c-365">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a462c-366">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="a462c-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="a462c-367">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-367">No new cmdlets are added.</span></span> <span data-ttu-id="a462c-368">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="a462c-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-370">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-371">Az.Resources</span></span>
* <span data-ttu-id="a462c-372">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="a462c-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="a462c-373">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a462c-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="a462c-374">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a462c-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="a462c-375">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="a462c-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="a462c-376">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="a462c-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="a462c-377">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="a462c-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="a462c-378">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="a462c-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="a462c-379">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="a462c-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-380">Az.Sql</span></span>
* <span data-ttu-id="a462c-381">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="a462c-382">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="a462c-383">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="a462c-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a462c-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a462c-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a462c-385">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a462c-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a462c-386">Az.StorageSync</span></span>
* <span data-ttu-id="a462c-387">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="a462c-388">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="a462c-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a462c-389">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a462c-389">Highlights since the last major release</span></span>
* <span data-ttu-id="a462c-390">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="a462c-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="a462c-391">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-392">Az.Accounts</span></span>
* <span data-ttu-id="a462c-393">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="a462c-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="a462c-394">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="a462c-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a462c-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-395">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-396">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="a462c-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="a462c-397">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="a462c-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="a462c-398">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="a462c-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="a462c-399">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="a462c-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-400">Az.Compute</span></span>
* <span data-ttu-id="a462c-401">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="a462c-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="a462c-402">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="a462c-403">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="a462c-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="a462c-405">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-406">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-407">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a462c-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a462c-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="a462c-409">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="a462c-410">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a462c-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-411">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-412">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-413">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-414">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="a462c-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-415">Az.Network</span></span>
* <span data-ttu-id="a462c-416">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="a462c-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="a462c-417">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a462c-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="a462c-418">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="a462c-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a462c-419">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="a462c-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="a462c-420">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="a462c-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="a462c-421">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="a462c-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="a462c-422">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="a462c-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="a462c-423">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="a462c-424">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-424">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="a462c-426">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="a462c-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a462c-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="a462c-428">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-430">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a462c-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="a462c-431">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="a462c-432">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="a462c-433">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-435">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="a462c-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="a462c-436">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-437">Az.Resources</span></span>
* <span data-ttu-id="a462c-438">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="a462c-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="a462c-439">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-440">Az.Sql</span></span>
<span data-ttu-id="a462c-441">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="a462c-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-442">Az.Storage</span></span>
* <span data-ttu-id="a462c-443">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a462c-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="a462c-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="a462c-445">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="a462c-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="a462c-446">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-447">Az.Websites</span></span>
* <span data-ttu-id="a462c-448">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="a462c-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="a462c-449">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="a462c-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="a462c-450">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="a462c-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-451">Az.Accounts</span></span>
* <span data-ttu-id="a462c-452">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="a462c-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-453">Az.Cdn</span></span>
* <span data-ttu-id="a462c-454">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="a462c-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-455">Az.Compute</span></span>
* <span data-ttu-id="a462c-456">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a462c-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="a462c-458">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a462c-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a462c-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a462c-460">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a462c-461">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="a462c-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="a462c-462">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a462c-463">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="a462c-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="a462c-464">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a462c-465">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="a462c-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="a462c-466">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a462c-467">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="a462c-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="a462c-468">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a462c-469">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="a462c-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="a462c-470">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a462c-471">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="a462c-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="a462c-472">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a462c-473">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="a462c-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="a462c-474">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="a462c-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="a462c-475">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="a462c-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="a462c-476">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="a462c-477">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="a462c-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-478">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-479">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="a462c-480">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="a462c-481">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a462c-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="a462c-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a462c-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="a462c-483">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-484">Az.EventHub</span></span>
* <span data-ttu-id="a462c-485">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a462c-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-486">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-487">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a462c-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a462c-488">Az.MachineLearning</span></span>
* <span data-ttu-id="a462c-489">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a462c-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="a462c-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a462c-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="a462c-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a462c-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="a462c-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a462c-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="a462c-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a462c-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="a462c-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a462c-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="a462c-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="a462c-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="a462c-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="a462c-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-497">Az.Network</span></span>
* <span data-ttu-id="a462c-498">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="a462c-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-500">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="a462c-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="a462c-501">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="a462c-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a462c-502">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="a462c-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a462c-503">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="a462c-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-504">Az.Resources</span></span>
* <span data-ttu-id="a462c-505">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-506">Az.Sql</span></span>
* <span data-ttu-id="a462c-507">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="a462c-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="a462c-508">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a462c-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a462c-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a462c-510">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-511">Az.Storage</span></span>
* <span data-ttu-id="a462c-512">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="a462c-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="a462c-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="a462c-514">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="a462c-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="a462c-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="a462c-516">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="a462c-517">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-517">General</span></span>
* <span data-ttu-id="a462c-518">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-519">Az.Accounts</span></span>
* <span data-ttu-id="a462c-520">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="a462c-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="a462c-521">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="a462c-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a462c-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a462c-522">Az.Batch</span></span>
* <span data-ttu-id="a462c-523">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="a462c-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-524">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-525">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a462c-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-526">Az.FrontDoor</span></span>
* <span data-ttu-id="a462c-527">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="a462c-528">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a462c-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a462c-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="a462c-530">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="a462c-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-531">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-532">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="a462c-533">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="a462c-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="a462c-534">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-535">Az.Monitor</span></span>
* <span data-ttu-id="a462c-536">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="a462c-537">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="a462c-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="a462c-538">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="a462c-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-539">Az.Network</span></span>
* <span data-ttu-id="a462c-540">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="a462c-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-541">Az.Resources</span></span>
* <span data-ttu-id="a462c-542">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="a462c-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="a462c-543">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="a462c-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-544">Az.Sql</span></span>
* <span data-ttu-id="a462c-545">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-546">Az.Storage</span></span>
* <span data-ttu-id="a462c-547">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a462c-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="a462c-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a462c-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="a462c-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a462c-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="a462c-550">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="a462c-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="a462c-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="a462c-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="a462c-552">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a462c-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="a462c-553">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="a462c-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a462c-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="a462c-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a462c-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="a462c-556">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="a462c-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a462c-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="a462c-558">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="a462c-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="a462c-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a462c-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="a462c-560">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a462c-561">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a462c-561">Highlights since the last major release</span></span>
* <span data-ttu-id="a462c-562">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="a462c-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="a462c-563">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="a462c-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-564">Az.Compute</span></span>
* <span data-ttu-id="a462c-565">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="a462c-565">VM Reapply feature</span></span>
    - <span data-ttu-id="a462c-566">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="a462c-567">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="a462c-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="a462c-568">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a462c-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="a462c-569">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="a462c-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="a462c-570">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a462c-571">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="a462c-572">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="a462c-573">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="a462c-574">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="a462c-575">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a462c-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a462c-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a462c-577">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a462c-578">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="a462c-578">Get the Order</span></span>
* <span data-ttu-id="a462c-579">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a462c-580">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="a462c-580">Create new Order</span></span>
* <span data-ttu-id="a462c-581">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a462c-582">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="a462c-582">Remove the Order</span></span>
* <span data-ttu-id="a462c-583">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="a462c-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="a462c-584">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="a462c-584">Now creates Local Share</span></span>
* <span data-ttu-id="a462c-585">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="a462c-586">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="a462c-587">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="a462c-588">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="a462c-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="a462c-589">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a462c-590">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="a462c-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="a462c-591">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a462c-592">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="a462c-592">Create new Triggers</span></span>
* <span data-ttu-id="a462c-593">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a462c-594">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="a462c-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-595">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-596">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="a462c-597">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a462c-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-599">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-600">Az.EventHub</span></span>
* <span data-ttu-id="a462c-601">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a462c-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-602">Az.FrontDoor</span></span>
* <span data-ttu-id="a462c-603">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="a462c-604">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="a462c-605">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="a462c-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="a462c-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-607">Az.Network</span></span>
* <span data-ttu-id="a462c-608">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a462c-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a462c-609">Az.PrivateDns</span></span>
* <span data-ttu-id="a462c-610">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-612">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="a462c-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="a462c-613">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="a462c-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="a462c-614">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="a462c-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a462c-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a462c-615">Az.RedisCache</span></span>
* <span data-ttu-id="a462c-616">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="a462c-617">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="a462c-618">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-619">Az.Resources</span></span>
- <span data-ttu-id="a462c-620">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a462c-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="a462c-621">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="a462c-622">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="a462c-623">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="a462c-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="a462c-624">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a462c-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-625">Az.Sql</span></span>
* <span data-ttu-id="a462c-626">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="a462c-627">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="a462c-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="a462c-628">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="a462c-629">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-629">General</span></span>
* <span data-ttu-id="a462c-630">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a462c-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-631">Az.Accounts</span></span>
* <span data-ttu-id="a462c-632">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a462c-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a462c-633">Az.Advisor</span></span>
* <span data-ttu-id="a462c-634">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a462c-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a462c-635">Az.Batch</span></span>
* <span data-ttu-id="a462c-636">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a462c-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="a462c-637">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="a462c-638">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="a462c-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="a462c-639">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="a462c-640">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="a462c-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="a462c-641">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="a462c-642">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a462c-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="a462c-643">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="a462c-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="a462c-644">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="a462c-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="a462c-645">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a462c-646">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="a462c-647">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="a462c-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="a462c-648">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a462c-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a462c-649">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="a462c-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="a462c-650">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="a462c-651">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a462c-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="a462c-652">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a462c-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="a462c-653">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="a462c-654">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="a462c-655">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a462c-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="a462c-656">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a462c-657">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a462c-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a462c-658">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="a462c-659">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a462c-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="a462c-660">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="a462c-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="a462c-661">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a462c-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="a462c-662">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a462c-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="a462c-663">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="a462c-664">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="a462c-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="a462c-665">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="a462c-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="a462c-666">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a462c-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="a462c-667">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="a462c-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="a462c-668">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="a462c-669">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a462c-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="a462c-670">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="a462c-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="a462c-671">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="a462c-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-672">Az.Cdn</span></span>
* <span data-ttu-id="a462c-673">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a462c-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="a462c-674">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="a462c-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-675">Az.Compute</span></span>
* <span data-ttu-id="a462c-676">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="a462c-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="a462c-677">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a462c-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="a462c-678">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a462c-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="a462c-679">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a462c-680">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="a462c-681">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="a462c-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="a462c-682">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="a462c-683">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="a462c-683">Breaking changes</span></span>
    - <span data-ttu-id="a462c-684">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a462c-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="a462c-685">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a462c-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-686">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-687">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-689">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="a462c-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="a462c-690">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="a462c-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="a462c-691">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="a462c-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="a462c-692">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="a462c-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="a462c-693">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="a462c-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="a462c-694">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="a462c-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a462c-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-695">Az.FrontDoor</span></span>
* <span data-ttu-id="a462c-696">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a462c-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-697">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-698">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="a462c-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="a462c-699">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a462c-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="a462c-700">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="a462c-701">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="a462c-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="a462c-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a462c-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a462c-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a462c-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a462c-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a462c-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a462c-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a462c-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="a462c-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a462c-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="a462c-707">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="a462c-708">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="a462c-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a462c-709">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="a462c-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a462c-710">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="a462c-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="a462c-711">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a462c-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="a462c-712">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="a462c-713">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="a462c-714">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="a462c-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="a462c-715">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="a462c-716">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="a462c-717">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="a462c-718">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="a462c-719">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="a462c-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-720">Az.IotHub</span></span>
* <span data-ttu-id="a462c-721">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="a462c-721">Breaking changes:</span></span>
    - <span data-ttu-id="a462c-722">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a462c-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a462c-723">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a462c-724">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a462c-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a462c-725">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a462c-726">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="a462c-727">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="a462c-728">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="a462c-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="a462c-729">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="a462c-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="a462c-730">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a462c-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a462c-731">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a462c-732">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a462c-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a462c-733">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-735">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-736">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="a462c-737">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="a462c-738">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-739">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-740">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-741">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-742">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-743">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-744">Az.Resources</span></span>
* <span data-ttu-id="a462c-745">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-746">Az.Network</span></span>
* <span data-ttu-id="a462c-747">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a462c-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="a462c-748">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a462c-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="a462c-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a462c-754">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="a462c-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="a462c-755">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a462c-755">New cmdlet:</span></span>
        - <span data-ttu-id="a462c-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a462c-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="a462c-757">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="a462c-758">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="a462c-759">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="a462c-760">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a462c-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="a462c-761">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="a462c-762">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="a462c-763">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="a462c-764">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-764">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a462c-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="a462c-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a462c-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a462c-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a462c-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a462c-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a462c-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a462c-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a462c-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="a462c-770">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="a462c-771">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a462c-772">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a462c-773">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a462c-774">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="a462c-775">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="a462c-776">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="a462c-777">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-777">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="a462c-779">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a462c-780">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a462c-781">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a462c-782">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a462c-783">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a462c-784">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="a462c-785">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="a462c-786">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-786">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a462c-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="a462c-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="a462c-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="a462c-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a462c-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="a462c-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a462c-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="a462c-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a462c-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="a462c-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="a462c-793">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a462c-794">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="a462c-795">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="a462c-796">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="a462c-797">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="a462c-798">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a462c-799">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="a462c-800">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="a462c-801">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="a462c-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="a462c-802">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="a462c-803">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="a462c-804">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-804">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a462c-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="a462c-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a462c-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="a462c-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a462c-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="a462c-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a462c-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-810">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="a462c-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-811">Az.Sql</span></span>
* <span data-ttu-id="a462c-812">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="a462c-813">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="a462c-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="a462c-814">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="a462c-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="a462c-815">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="a462c-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="a462c-816">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="a462c-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="a462c-817">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a462c-818">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="a462c-819">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="a462c-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="a462c-820">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-821">Az.Storage</span></span>
* <span data-ttu-id="a462c-822">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="a462c-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a462c-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a462c-825">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a462c-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="a462c-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a462c-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="a462c-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a462c-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="a462c-828">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a462c-829">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-829">General</span></span>
* <span data-ttu-id="a462c-830">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a462c-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-831">Az.Accounts</span></span>
* <span data-ttu-id="a462c-832">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a462c-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-833">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-834">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a462c-835">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="a462c-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-836">Az.Automation</span></span>
* <span data-ttu-id="a462c-837">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a462c-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a462c-838">Az.Batch</span></span>
* <span data-ttu-id="a462c-839">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a462c-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-840">Az.Compute</span></span>
* <span data-ttu-id="a462c-841">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a462c-842">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a462c-843">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="a462c-844">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="a462c-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-845">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-846">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="a462c-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a462c-847">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a462c-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a462c-848">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-850">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="a462c-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a462c-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a462c-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="a462c-852">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a462c-853">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a462c-854">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="a462c-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a462c-855">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-856">Az.IotHub</span></span>
* <span data-ttu-id="a462c-857">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="a462c-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a462c-858">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="a462c-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-859">Az.Monitor</span></span>
* <span data-ttu-id="a462c-860">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a462c-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a462c-861">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a462c-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a462c-862">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="a462c-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a462c-863">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="a462c-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-864">Az.Network</span></span>
* <span data-ttu-id="a462c-865">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="a462c-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a462c-866">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a462c-867">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-867">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a462c-869">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a462c-870">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a462c-871">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="a462c-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a462c-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a462c-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a462c-875">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a462c-876">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a462c-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a462c-877">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a462c-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a462c-878">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a462c-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a462c-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a462c-879">Az.RedisCache</span></span>
* <span data-ttu-id="a462c-880">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="a462c-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-881">Az.Sql</span></span>
* <span data-ttu-id="a462c-882">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-883">Az.Storage</span></span>
* <span data-ttu-id="a462c-884">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a462c-885">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="a462c-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a462c-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a462c-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a462c-887">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="a462c-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a462c-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a462c-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a462c-889">Az.StorageSync</span></span>
* <span data-ttu-id="a462c-890">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-891">Az.Websites</span></span>
* <span data-ttu-id="a462c-892">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="a462c-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a462c-893">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a462c-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-894">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-895">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a462c-896">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a462c-897">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="a462c-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-898">Az.Automation</span></span>
* <span data-ttu-id="a462c-899">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a462c-900">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a462c-901">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-902">Az.Compute</span></span>
* <span data-ttu-id="a462c-903">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a462c-904">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a462c-905">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a462c-906">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a462c-907">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a462c-908">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="a462c-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a462c-909">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a462c-910">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a462c-911">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-912">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-913">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a462c-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a462c-914">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a462c-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-915">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-916">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-917">Az.IotHub</span></span>
* <span data-ttu-id="a462c-918">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a462c-919">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a462c-920">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="a462c-920">New cmdlets are:</span></span>
    - <span data-ttu-id="a462c-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a462c-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a462c-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a462c-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a462c-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a462c-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a462c-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a462c-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-925">Az.Monitor</span></span>
* <span data-ttu-id="a462c-926">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="a462c-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a462c-927">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="a462c-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a462c-928">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a462c-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a462c-929">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="a462c-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a462c-930">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="a462c-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a462c-931">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="a462c-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a462c-932">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a462c-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a462c-933">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a462c-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a462c-934">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a462c-935">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a462c-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a462c-936">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a462c-937">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a462c-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a462c-938">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="a462c-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a462c-939">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="a462c-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a462c-940">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="a462c-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a462c-941">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="a462c-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a462c-942">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="a462c-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a462c-943">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="a462c-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a462c-944">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a462c-945">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="a462c-945">Overall improved help files</span></span>
* <span data-ttu-id="a462c-946">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-947">Az.Network</span></span>
* <span data-ttu-id="a462c-948">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="a462c-949">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a462c-950">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="a462c-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a462c-951">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="a462c-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a462c-952">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a462c-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a462c-953">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a462c-954">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a462c-955">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a462c-956">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a462c-957">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a462c-958">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a462c-959">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="a462c-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a462c-960">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-960">New cmdlets</span></span>
        - <span data-ttu-id="a462c-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a462c-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a462c-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a462c-963">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a462c-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="a462c-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a462c-964">New-VpnSite</span></span>
        - <span data-ttu-id="a462c-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a462c-965">Update-VpnSite</span></span>
        - <span data-ttu-id="a462c-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-966">New-VpnConnection</span></span>
        - <span data-ttu-id="a462c-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-967">Update-VpnConnection</span></span>
* <span data-ttu-id="a462c-968">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a462c-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-970">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a462c-971">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-972">Az.Resources</span></span>
* <span data-ttu-id="a462c-973">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="a462c-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-975">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a462c-976">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a462c-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a462c-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a462c-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a462c-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a462c-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a462c-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a462c-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a462c-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a462c-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a462c-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a462c-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a462c-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a462c-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a462c-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a462c-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a462c-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a462c-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a462c-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a462c-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a462c-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a462c-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a462c-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a462c-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a462c-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a462c-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a462c-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a462c-990">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="a462c-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a462c-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a462c-991">Az.SignalR</span></span>
* <span data-ttu-id="a462c-992">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-993">Az.Sql</span></span>
* <span data-ttu-id="a462c-994">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a462c-995">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="a462c-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a462c-996">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="a462c-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a462c-997">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a462c-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a462c-998">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="a462c-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-999">Az.Storage</span></span>
* <span data-ttu-id="a462c-1000">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a462c-1001">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a462c-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a462c-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a462c-1004">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a462c-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a462c-1006">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="a462c-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a462c-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a462c-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a462c-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a462c-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a462c-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a462c-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a462c-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a462c-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1011">Az.Websites</span></span>
* <span data-ttu-id="a462c-1012">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="a462c-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a462c-1013">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a462c-1014">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a462c-1015">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a462c-1016">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-1016">General</span></span>
* <span data-ttu-id="a462c-1017">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1018">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1019">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="a462c-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a462c-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a462c-1020">Az.Aks</span></span>
* <span data-ttu-id="a462c-1021">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a462c-1022">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a462c-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a462c-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-1024">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a462c-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a462c-1025">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="a462c-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a462c-1026">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a462c-1027">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a462c-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a462c-1028">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a462c-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a462c-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a462c-1029">Az.Batch</span></span>
* <span data-ttu-id="a462c-1030">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="a462c-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-1031">Az.Cdn</span></span>
* <span data-ttu-id="a462c-1032">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1033">Az.Compute</span></span>
* <span data-ttu-id="a462c-1034">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a462c-1035">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a462c-1036">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a462c-1037">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a462c-1038">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a462c-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a462c-1039">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a462c-1040">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a462c-1041">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1042">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1043">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="a462c-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a462c-1044">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a462c-1045">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a462c-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a462c-1046">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-1048">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1049">Az.EventHub</span></span>
* <span data-ttu-id="a462c-1050">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="a462c-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a462c-1051">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="a462c-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a462c-1052">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a462c-1053">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a462c-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a462c-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a462c-1055">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-1056">Az.Monitor</span></span>
* <span data-ttu-id="a462c-1057">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1058">Az.Network</span></span>
* <span data-ttu-id="a462c-1059">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a462c-1060">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="a462c-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a462c-1061">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="a462c-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a462c-1062">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a462c-1063">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="a462c-1064">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a462c-1065">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="a462c-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="a462c-1067">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="a462c-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a462c-1068">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1068">Added example</span></span>
    - <span data-ttu-id="a462c-1069">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a462c-1070">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a462c-1071">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1073">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1074">Az.Resources</span></span>
* <span data-ttu-id="a462c-1075">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a462c-1076">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a462c-1077">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a462c-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a462c-1078">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a462c-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a462c-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="a462c-1080">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="a462c-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a462c-1081">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a462c-1082">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-1084">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="a462c-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a462c-1085">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="a462c-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a462c-1086">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a462c-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a462c-1087">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="a462c-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a462c-1088">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a462c-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a462c-1089">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="a462c-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1090">Az.Sql</span></span>
* <span data-ttu-id="a462c-1091">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1092">Az.Storage</span></span>
* <span data-ttu-id="a462c-1093">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="a462c-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a462c-1094">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="a462c-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a462c-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a462c-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a462c-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a462c-1097">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="a462c-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a462c-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a462c-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1099">Az.Websites</span></span>
* <span data-ttu-id="a462c-1100">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="a462c-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a462c-1101">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1102">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1103">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a462c-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a462c-1105">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1106">Az.Automation</span></span>
* <span data-ttu-id="a462c-1107">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-1109">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1110">Az.Compute</span></span>
* <span data-ttu-id="a462c-1111">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a462c-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a462c-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a462c-1113">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a462c-1114">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="a462c-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1115">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1116">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a462c-1117">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1118">Az.EventHub</span></span>
* <span data-ttu-id="a462c-1119">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a462c-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a462c-1120">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-1121">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-1122">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a462c-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a462c-1123">Az.LogicApp</span></span>
* <span data-ttu-id="a462c-1124">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="a462c-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a462c-1125">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a462c-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="a462c-1127">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1128">Az.Network</span></span>
* <span data-ttu-id="a462c-1129">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a462c-1130">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1130">New cmdlets</span></span>
        - <span data-ttu-id="a462c-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a462c-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a462c-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a462c-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a462c-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a462c-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a462c-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a462c-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a462c-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a462c-1139">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a462c-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a462c-1140">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a462c-1141">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a462c-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a462c-1142">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a462c-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a462c-1143">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a462c-1144">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="a462c-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a462c-1145">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="a462c-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a462c-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a462c-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a462c-1149">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a462c-1150">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a462c-1151">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a462c-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="a462c-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a462c-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a462c-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a462c-1155">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a462c-1156">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a462c-1157">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="a462c-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="a462c-1159">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="a462c-1160">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1162">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a462c-1163">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a462c-1164">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a462c-1165">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a462c-1166">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a462c-1167">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a462c-1168">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a462c-1169">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a462c-1170">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a462c-1171">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1172">Az.Resources</span></span>
- <span data-ttu-id="a462c-1173">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a462c-1174">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a462c-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a462c-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="a462c-1176">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a462c-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a462c-1177">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1178">Az.Sql</span></span>
* <span data-ttu-id="a462c-1179">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a462c-1180">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a462c-1181">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1182">Az.Storage</span></span>
* <span data-ttu-id="a462c-1183">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a462c-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a462c-1184">Az.StorageSync</span></span>
* <span data-ttu-id="a462c-1185">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a462c-1186">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1187">Az.Websites</span></span>
* <span data-ttu-id="a462c-1188">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="a462c-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a462c-1189">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a462c-1190">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a462c-1191">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1192">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1193">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a462c-1194">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a462c-1195">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="a462c-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a462c-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a462c-1196">Az.Advisor</span></span>
* <span data-ttu-id="a462c-1197">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a462c-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a462c-1198">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="a462c-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a462c-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-1200">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a462c-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a462c-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a462c-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a462c-1202">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a462c-1203">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="a462c-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a462c-1204">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a462c-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a462c-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a462c-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a462c-1206">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1207">Az.Automation</span></span>
* <span data-ttu-id="a462c-1208">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1209">Az.Compute</span></span>
* <span data-ttu-id="a462c-1210">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1211">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1212">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a462c-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a462c-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a462c-1213">Az.EventGrid</span></span>
* <span data-ttu-id="a462c-1214">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1215">Az.IotHub</span></span>
* <span data-ttu-id="a462c-1216">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1217">Az.Network</span></span>
* <span data-ttu-id="a462c-1218">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a462c-1219">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a462c-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-1221">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a462c-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a462c-1222">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a462c-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="a462c-1224">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1226">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="a462c-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1227">Az.Resources</span></span>
    - <span data-ttu-id="a462c-1228">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a462c-1229">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a462c-1230">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a462c-1231">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a462c-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a462c-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="a462c-1233">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="a462c-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1234">Az.Sql</span></span>
* <span data-ttu-id="a462c-1235">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a462c-1236">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a462c-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a462c-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a462c-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a462c-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a462c-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a462c-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a462c-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a462c-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a462c-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a462c-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a462c-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a462c-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a462c-1243">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1244">Az.Storage</span></span>
* <span data-ttu-id="a462c-1245">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="a462c-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a462c-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a462c-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a462c-1247">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="a462c-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a462c-1248">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="a462c-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a462c-1249">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a462c-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a462c-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a462c-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a462c-1252">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="a462c-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a462c-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a462c-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a462c-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a462c-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a462c-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a462c-1255">Az.StorageSync</span></span>
* <span data-ttu-id="a462c-1256">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="a462c-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a462c-1257">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1258">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1259">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="a462c-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a462c-1260">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a462c-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a462c-1261">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a462c-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a462c-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a462c-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a462c-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1264">Az.Compute</span></span>
* <span data-ttu-id="a462c-1265">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="a462c-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a462c-1266">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a462c-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a462c-1267">Az.Dns</span></span>
* <span data-ttu-id="a462c-1268">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a462c-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a462c-1269">Az.EventGrid</span></span>
* <span data-ttu-id="a462c-1270">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a462c-1271">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-1271">New cmdlets:</span></span>
    - <span data-ttu-id="a462c-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a462c-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a462c-1273">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="a462c-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a462c-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a462c-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a462c-1275">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a462c-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a462c-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a462c-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a462c-1277">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="a462c-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a462c-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a462c-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a462c-1279">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="a462c-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a462c-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a462c-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a462c-1281">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a462c-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a462c-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a462c-1283">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="a462c-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a462c-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a462c-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a462c-1285">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a462c-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="a462c-1286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a462c-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a462c-1287">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="a462c-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a462c-1288">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="a462c-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a462c-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a462c-1290">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a462c-1291">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a462c-1292">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="a462c-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a462c-1293">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a462c-1294">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="a462c-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a462c-1295">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="a462c-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a462c-1296">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a462c-1297">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="a462c-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="a462c-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a462c-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a462c-1299">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a462c-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a462c-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a462c-1301">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a462c-1302">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="a462c-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a462c-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="a462c-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a462c-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a462c-1305">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a462c-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a462c-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a462c-1307">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1308">Az.Network</span></span>
* <span data-ttu-id="a462c-1309">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a462c-1310">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1310">New cmdlets</span></span>
        - <span data-ttu-id="a462c-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a462c-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a462c-1312">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a462c-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a462c-1313">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1313">New cmdlets</span></span>
        - <span data-ttu-id="a462c-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a462c-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a462c-1315">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a462c-1316">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1316">New cmdlets</span></span>
        - <span data-ttu-id="a462c-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a462c-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a462c-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a462c-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a462c-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a462c-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a462c-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a462c-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a462c-1322">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a462c-1323">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1323">New cmdlets</span></span>
        - <span data-ttu-id="a462c-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a462c-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a462c-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a462c-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a462c-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a462c-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a462c-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a462c-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a462c-1328">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="a462c-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a462c-1329">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="a462c-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a462c-1330">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="a462c-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a462c-1331">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a462c-1332">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a462c-1333">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="a462c-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a462c-1334">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a462c-1335">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="a462c-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a462c-1336">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a462c-1337">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a462c-1338">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="a462c-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a462c-1339">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a462c-1340">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a462c-1341">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a462c-1342">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="a462c-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a462c-1343">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a462c-1344">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a462c-1345">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="a462c-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a462c-1346">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="a462c-1347">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="a462c-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="a462c-1348">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a462c-1349">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a462c-1350">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="a462c-1352">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="a462c-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1353">Az.Resources</span></span>
* <span data-ttu-id="a462c-1354">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a462c-1355">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a462c-1356">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a462c-1357">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a462c-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-1359">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="a462c-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1360">Az.Sql</span></span>
* <span data-ttu-id="a462c-1361">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a462c-1362">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a462c-1363">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="a462c-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a462c-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a462c-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a462c-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a462c-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a462c-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a462c-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a462c-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a462c-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a462c-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a462c-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1369">Az.Storage</span></span>
* <span data-ttu-id="a462c-1370">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a462c-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a462c-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="a462c-1372">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="a462c-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a462c-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1374">Az.Websites</span></span>
* <span data-ttu-id="a462c-1375">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="a462c-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a462c-1376">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a462c-1377">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a462c-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-1378">Az.Cdn</span></span>
* <span data-ttu-id="a462c-1379">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a462c-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1380">Az.Compute</span></span>
* <span data-ttu-id="a462c-1381">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a462c-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a462c-1382">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a462c-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1383">Az.EventHub</span></span>
* <span data-ttu-id="a462c-1384">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="a462c-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a462c-1385">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="a462c-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1386">Az.Network</span></span>
* <span data-ttu-id="a462c-1387">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a462c-1388">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-1390">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a462c-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1392">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a462c-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a462c-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="a462c-1394">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="a462c-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-1396">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a462c-1397">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1398">Az.Sql</span></span>
* <span data-ttu-id="a462c-1399">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a462c-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a462c-1400">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a462c-1401">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="a462c-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a462c-1402">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="a462c-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1403">Az.Websites</span></span>
* <span data-ttu-id="a462c-1404">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a462c-1405">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a462c-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-1407">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a462c-1408">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="a462c-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a462c-1409">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a462c-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a462c-1410">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="a462c-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a462c-1411">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="a462c-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a462c-1412">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="a462c-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a462c-1413">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a462c-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a462c-1414">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a462c-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a462c-1415">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a462c-1416">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="a462c-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a462c-1417">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="a462c-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a462c-1418">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="a462c-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a462c-1419">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="a462c-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a462c-1420">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a462c-1421">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="a462c-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a462c-1422">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="a462c-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a462c-1423">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="a462c-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a462c-1424">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="a462c-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a462c-1425">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="a462c-1426">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="a462c-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a462c-1427">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a462c-1428">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="a462c-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a462c-1429">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="a462c-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a462c-1430">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="a462c-1431">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a462c-1432">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a462c-1433">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="a462c-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a462c-1434">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a462c-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a462c-1435">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a462c-1436">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="a462c-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a462c-1437">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="a462c-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="a462c-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a462c-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a462c-1439">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a462c-1440">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a462c-1441">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="a462c-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a462c-1442">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a462c-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a462c-1443">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a462c-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a462c-1444">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="a462c-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a462c-1445">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="a462c-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a462c-1446">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a462c-1447">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="a462c-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a462c-1448">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="a462c-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a462c-1449">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="a462c-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a462c-1450">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a462c-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a462c-1451">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a462c-1452">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="a462c-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a462c-1453">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="a462c-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a462c-1454">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="a462c-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a462c-1455">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a462c-1456">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="a462c-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a462c-1457">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="a462c-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a462c-1458">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="a462c-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a462c-1459">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="a462c-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a462c-1460">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a462c-1461">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="a462c-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a462c-1462">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="a462c-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a462c-1463">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a462c-1464">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a462c-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a462c-1465">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a462c-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a462c-1466">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a462c-1467">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a462c-1468">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a462c-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a462c-1469">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="a462c-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a462c-1470">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a462c-1471">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="a462c-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a462c-1472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="a462c-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a462c-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a462c-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a462c-1474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="a462c-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a462c-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a462c-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a462c-1476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a462c-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a462c-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a462c-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a462c-1478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a462c-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a462c-1479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="a462c-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a462c-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a462c-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a462c-1481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="a462c-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="a462c-1482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a462c-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a462c-1483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="a462c-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1484">Az.Automation</span></span>
* <span data-ttu-id="a462c-1485">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a462c-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a462c-1486">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a462c-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a462c-1487">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a462c-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a462c-1488">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="a462c-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a462c-1489">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a462c-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a462c-1490">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="a462c-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a462c-1491">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="a462c-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1492">Az.Compute</span></span>
* <span data-ttu-id="a462c-1493">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a462c-1494">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-1496">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="a462c-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-1497">Az.Monitor</span></span>
* <span data-ttu-id="a462c-1498">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="a462c-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1499">Az.Network</span></span>
* <span data-ttu-id="a462c-1500">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a462c-1501">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a462c-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="a462c-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a462c-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a462c-1503">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a462c-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1504">Az.Resources</span></span>
* <span data-ttu-id="a462c-1505">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1506">Az.Sql</span></span>
* <span data-ttu-id="a462c-1507">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="a462c-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a462c-1508">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1509">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1510">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="a462c-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-1512">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="a462c-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a462c-1513">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="a462c-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1514">Az.Compute</span></span>
* <span data-ttu-id="a462c-1515">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a462c-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a462c-1516">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a462c-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a462c-1517">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a462c-1518">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a462c-1519">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="a462c-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a462c-1520">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="a462c-1521">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="a462c-1521">Breaking changes</span></span>
    - <span data-ttu-id="a462c-1522">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a462c-1523">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a462c-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a462c-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="a462c-1525">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a462c-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a462c-1526">Az.Dns</span></span>
* <span data-ttu-id="a462c-1527">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="a462c-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a462c-1528">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="a462c-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a462c-1529">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a462c-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="a462c-1531">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a462c-1532">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="a462c-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a462c-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-1533">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-1534">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="a462c-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a462c-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a462c-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a462c-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a462c-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a462c-1537">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="a462c-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a462c-1538">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="a462c-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a462c-1539">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a462c-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a462c-1540">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="a462c-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-1541">Az.Monitor</span></span>
* <span data-ttu-id="a462c-1542">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="a462c-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="a462c-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a462c-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a462c-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a462c-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a462c-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a462c-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a462c-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a462c-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a462c-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a462c-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a462c-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a462c-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a462c-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a462c-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a462c-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a462c-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a462c-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a462c-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a462c-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a462c-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a462c-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a462c-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a462c-1554">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="a462c-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a462c-1555">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="a462c-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1556">Az.Network</span></span>
* <span data-ttu-id="a462c-1557">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a462c-1558">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1558">New cmdlets</span></span>
        - <span data-ttu-id="a462c-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="a462c-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a462c-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a462c-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a462c-1563">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="a462c-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a462c-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a462c-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a462c-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a462c-1566">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a462c-1567">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="a462c-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a462c-1568">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="a462c-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-1570">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="a462c-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a462c-1571">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a462c-1572">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="a462c-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1574">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="a462c-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a462c-1575">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="a462c-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a462c-1576">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="a462c-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a462c-1577">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="a462c-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a462c-1578">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="a462c-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a462c-1579">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="a462c-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a462c-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a462c-1580">Az.Relay</span></span>
* <span data-ttu-id="a462c-1581">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="a462c-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a462c-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a462c-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="a462c-1583">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1584">Az.Storage</span></span>
* <span data-ttu-id="a462c-1585">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="a462c-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a462c-1586">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a462c-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a462c-1587">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a462c-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="a462c-1589">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="a462c-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a462c-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a462c-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a462c-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1593">Az.Websites</span></span>
* <span data-ttu-id="a462c-1594">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a462c-1595">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a462c-1596">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a462c-1597">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a462c-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="a462c-1598">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="a462c-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="a462c-1599">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="a462c-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a462c-1600">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="a462c-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a462c-1601">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a462c-1602">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a462c-1603">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a462c-1604">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1605">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1606">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="a462c-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a462c-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a462c-1607">Az.Batch</span></span>
* <span data-ttu-id="a462c-1608">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-1609">Az.Cdn</span></span>
* <span data-ttu-id="a462c-1610">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-1612">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1613">Az.Compute</span></span>
* <span data-ttu-id="a462c-1614">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="a462c-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a462c-1615">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a462c-1616">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1617">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1618">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="a462c-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-1620">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a462c-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a462c-1621">Az.EventGrid</span></span>
* <span data-ttu-id="a462c-1622">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a462c-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1623">Az.EventHub</span></span>
* <span data-ttu-id="a462c-1624">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a462c-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a462c-1625">Az.HDInsight</span></span>
* <span data-ttu-id="a462c-1626">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1627">Az.IotHub</span></span>
* <span data-ttu-id="a462c-1628">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-1629">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-1630">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a462c-1631">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a462c-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a462c-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="a462c-1633">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a462c-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a462c-1634">Az.Media</span></span>
* <span data-ttu-id="a462c-1635">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-1636">Az.Monitor</span></span>
  * <span data-ttu-id="a462c-1637">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="a462c-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a462c-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a462c-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a462c-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a462c-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a462c-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a462c-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a462c-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a462c-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a462c-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a462c-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a462c-1643">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1644">Az.Network</span></span>
* <span data-ttu-id="a462c-1645">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a462c-1646">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a462c-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a462c-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="a462c-1648">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="a462c-1650">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a462c-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a462c-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a462c-1652">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1654">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a462c-1655">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a462c-1656">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a462c-1657">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a462c-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a462c-1658">Az.RedisCache</span></span>
* <span data-ttu-id="a462c-1659">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1660">Az.Resources</span></span>
* <span data-ttu-id="a462c-1661">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1662">Az.Sql</span></span>
* <span data-ttu-id="a462c-1663">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="a462c-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a462c-1664">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a462c-1665">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="a462c-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a462c-1666">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a462c-1667">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="a462c-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a462c-1668">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="a462c-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a462c-1669">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1670">Az.Websites</span></span>
* <span data-ttu-id="a462c-1671">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="a462c-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a462c-1672">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a462c-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a462c-1673">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a462c-1674">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a462c-1675">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a462c-1676">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a462c-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="a462c-1677">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="a462c-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="a462c-1678">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="a462c-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a462c-1679">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="a462c-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a462c-1680">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a462c-1681">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a462c-1682">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a462c-1683">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a462c-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1684">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1685">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="a462c-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a462c-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="a462c-1687">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a462c-1688">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1689">Az.Automation</span></span>
* <span data-ttu-id="a462c-1690">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="a462c-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a462c-1691">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a462c-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a462c-1692">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="a462c-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1693">Az.Compute</span></span>
* <span data-ttu-id="a462c-1694">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a462c-1695">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="a462c-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a462c-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="a462c-1697">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="a462c-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1698">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1699">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a462c-1700">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1701">Az.Resources</span></span>
* <span data-ttu-id="a462c-1702">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a462c-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a462c-1703">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a462c-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a462c-1704">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="a462c-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a462c-1705">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a462c-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a462c-1706">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="a462c-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a462c-1707">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a462c-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1708">Az.Sql</span></span>
* <span data-ttu-id="a462c-1709">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="a462c-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1710">Az.Storage</span></span>
* <span data-ttu-id="a462c-1711">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="a462c-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a462c-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a462c-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="a462c-1713">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="a462c-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a462c-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a462c-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a462c-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a462c-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a462c-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a462c-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a462c-1718">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="a462c-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a462c-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a462c-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a462c-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a462c-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a462c-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a462c-1723">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a462c-1724">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a462c-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="a462c-1725">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="a462c-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="a462c-1726">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="a462c-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a462c-1727">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="a462c-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a462c-1728">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a462c-1729">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a462c-1730">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a462c-1731">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1732">Az.Automation</span></span>
* <span data-ttu-id="a462c-1733">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="a462c-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a462c-1734">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="a462c-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="a462c-1735">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="a462c-1735">Pre-Post script</span></span>
    * <span data-ttu-id="a462c-1736">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="a462c-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1737">Az.Compute</span></span>
* <span data-ttu-id="a462c-1738">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a462c-1739">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-1740">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-1741">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1742">Az.Network</span></span>
* <span data-ttu-id="a462c-1743">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a462c-1744">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1746">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="a462c-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a462c-1747">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1748">Az.Resources</span></span>
* <span data-ttu-id="a462c-1749">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a462c-1750">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a462c-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1751">Az.Sql</span></span>
* <span data-ttu-id="a462c-1752">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a462c-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1753">Az.Storage</span></span>
* <span data-ttu-id="a462c-1754">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a462c-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a462c-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a462c-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a462c-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a462c-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a462c-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a462c-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a462c-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a462c-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a462c-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1761">Az.Websites</span></span>
* <span data-ttu-id="a462c-1762">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="a462c-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="a462c-1763">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1764">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1765">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a462c-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a462c-1766">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1767">Az.Automation</span></span>
* <span data-ttu-id="a462c-1768">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="a462c-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a462c-1769">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a462c-1770">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a462c-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-1771">Az.Cdn</span></span>
* <span data-ttu-id="a462c-1772">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="a462c-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1773">Az.Compute</span></span>
* <span data-ttu-id="a462c-1774">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1775">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1776">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a462c-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a462c-1777">Az.LogicApp</span></span>
* <span data-ttu-id="a462c-1778">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a462c-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1779">Az.Network</span></span>
* <span data-ttu-id="a462c-1780">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1782">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="a462c-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a462c-1783">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="a462c-1783">SDK Update</span></span>
* <span data-ttu-id="a462c-1784">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a462c-1785">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1786">Az.Resources</span></span>
* <span data-ttu-id="a462c-1787">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a462c-1788">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a462c-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a462c-1789">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a462c-1790">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a462c-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a462c-1791">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a462c-1792">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a462c-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1793">Az.Sql</span></span>
* <span data-ttu-id="a462c-1794">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a462c-1795">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1796">Az.Storage</span></span>
* <span data-ttu-id="a462c-1797">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a462c-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a462c-1798">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a462c-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="a462c-1800">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1801">Az.Automation</span></span>
* <span data-ttu-id="a462c-1802">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a462c-1803">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a462c-1804">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="a462c-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-1806">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1807">Az.Compute</span></span>
* <span data-ttu-id="a462c-1808">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a462c-1809">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a462c-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a462c-1810">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a462c-1811">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="a462c-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-1813">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a462c-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1814">Az.EventHub</span></span>
* <span data-ttu-id="a462c-1815">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-1816">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-1817">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a462c-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a462c-1818">Az.LogicApp</span></span>
* <span data-ttu-id="a462c-1819">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a462c-1820">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a462c-1821">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="a462c-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a462c-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a462c-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a462c-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a462c-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a462c-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a462c-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a462c-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a462c-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a462c-1826">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a462c-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a462c-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a462c-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a462c-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a462c-1831">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a462c-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-1832">Az.Monitor</span></span>
* <span data-ttu-id="a462c-1833">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1834">Az.Network</span></span>
* <span data-ttu-id="a462c-1835">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="a462c-1837">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a462c-1838">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="a462c-1839">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="a462c-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1840">Az.Resources</span></span>
* <span data-ttu-id="a462c-1841">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a462c-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a462c-1842">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a462c-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a462c-1843">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a462c-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a462c-1844">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="a462c-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1845">Az.Sql</span></span>
* <span data-ttu-id="a462c-1846">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a462c-1847">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="a462c-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1848">Az.Websites</span></span>
* <span data-ttu-id="a462c-1849">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a462c-1850">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1851">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1852">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="a462c-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a462c-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="a462c-1854">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="a462c-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1855">Az.Compute</span></span>
* <span data-ttu-id="a462c-1856">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a462c-1857">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a462c-1858">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="a462c-1860">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="a462c-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1861">Az.Resources</span></span>
* <span data-ttu-id="a462c-1862">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="a462c-1863">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a462c-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a462c-1864">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="a462c-1865">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a462c-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1866">Az.Sql</span></span>
* <span data-ttu-id="a462c-1867">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a462c-1868">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="a462c-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a462c-1869">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a462c-1870">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1871">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1872">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a462c-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a462c-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="a462c-1874">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="a462c-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="a462c-1876">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="a462c-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a462c-1877">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1878">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1879">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a462c-1880">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a462c-1881">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a462c-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a462c-1882">Az.Aks</span></span>
* <span data-ttu-id="a462c-1883">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a462c-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-1884">Az.Automation</span></span>
* <span data-ttu-id="a462c-1885">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a462c-1886">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a462c-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a462c-1887">Az.Cdn</span></span>
* <span data-ttu-id="a462c-1888">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1889">Az.Compute</span></span>
* <span data-ttu-id="a462c-1890">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a462c-1891">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a462c-1892">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a462c-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a462c-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a462c-1894">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a462c-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a462c-1895">Az.DataFactory</span></span>
* <span data-ttu-id="a462c-1896">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-1898">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a462c-1899">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a462c-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a462c-1900">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1901">Az.IotHub</span></span>
* <span data-ttu-id="a462c-1902">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a462c-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-1903">Az.KeyVault</span></span>
* <span data-ttu-id="a462c-1904">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-1905">Az.Network</span></span>
* <span data-ttu-id="a462c-1906">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1907">Az.Resources</span></span>
* <span data-ttu-id="a462c-1908">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a462c-1909">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="a462c-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a462c-1910">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="a462c-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a462c-1911">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a462c-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a462c-1912">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a462c-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a462c-1913">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a462c-1914">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a462c-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-1916">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a462c-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a462c-1917">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-1917">Fix some error messages.</span></span>
* <span data-ttu-id="a462c-1918">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="a462c-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a462c-1919">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a462c-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a462c-1920">Az.SignalR</span></span>
* <span data-ttu-id="a462c-1921">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1922">Az.Sql</span></span>
* <span data-ttu-id="a462c-1923">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a462c-1924">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a462c-1925">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="a462c-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a462c-1926">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="a462c-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1927">Az.Storage</span></span>
* <span data-ttu-id="a462c-1928">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a462c-1929">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a462c-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a462c-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a462c-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a462c-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a462c-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a462c-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="a462c-1933">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1934">Az.Websites</span></span>
* <span data-ttu-id="a462c-1935">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a462c-1936">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a462c-1937">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a462c-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a462c-1938">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="a462c-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a462c-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1939">Az.Accounts</span></span>
* <span data-ttu-id="a462c-1940">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-1941">Az.Compute</span></span>
* <span data-ttu-id="a462c-1942">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="a462c-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a462c-1943">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a462c-1944">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-1946">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="a462c-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a462c-1947">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a462c-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a462c-1948">Az.EventGrid</span></span>
* <span data-ttu-id="a462c-1949">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a462c-1950">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a462c-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a462c-1951">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a462c-1952">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="a462c-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a462c-1953">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a462c-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a462c-1954">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a462c-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a462c-1955">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a462c-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a462c-1956">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="a462c-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a462c-1957">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a462c-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a462c-1958">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a462c-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="a462c-1959">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a462c-1960">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="a462c-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a462c-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a462c-1961">Az.IotHub</span></span>
* <span data-ttu-id="a462c-1962">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a462c-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a462c-1963">Az.LogicApp</span></span>
* <span data-ttu-id="a462c-1964">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="a462c-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-1965">Az.Resources</span></span>
* <span data-ttu-id="a462c-1966">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a462c-1967">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a462c-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a462c-1968">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a462c-1969">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a462c-1970">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="a462c-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a462c-1971">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a462c-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a462c-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a462c-1972">Az.SignalR</span></span>
* <span data-ttu-id="a462c-1973">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-1974">Az.Sql</span></span>
* <span data-ttu-id="a462c-1975">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="a462c-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a462c-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-1976">Az.Storage</span></span>
* <span data-ttu-id="a462c-1977">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="a462c-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a462c-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a462c-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="a462c-1979">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="a462c-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a462c-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a462c-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-1981">Az.Websites</span></span>
* <span data-ttu-id="a462c-1982">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a462c-1983">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a462c-1984">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a462c-1985">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-1985">General</span></span>

- <span data-ttu-id="a462c-1986">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="a462c-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="a462c-1987">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="a462c-1987">Online help for each module</span></span>
- <span data-ttu-id="a462c-1988">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="a462c-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a462c-1989">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a462c-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a462c-1990">Az.Accounts</span></span>
- <span data-ttu-id="a462c-1991">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a462c-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="a462c-1992">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="a462c-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a462c-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="a462c-1994">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="a462c-1994">Fixes for #7002</span></span>
- <span data-ttu-id="a462c-1995">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a462c-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a462c-1996">Az.Batch</span></span>
- <span data-ttu-id="a462c-1997">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a462c-1998">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="a462c-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a462c-1999">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a462c-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a462c-2000">Az.Billing</span></span>
- <span data-ttu-id="a462c-2001">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a462c-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a462c-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="a462c-2003">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a462c-2004">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a462c-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="a462c-2006">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a462c-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a462c-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a462c-2008">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a462c-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="a462c-2010">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a462c-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a462c-2011">Az.Monitor</span></span>
- <span data-ttu-id="a462c-2012">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a462c-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a462c-2013">Az.KeyVault</span></span>
- <span data-ttu-id="a462c-2014">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a462c-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a462c-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="a462c-2016">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="a462c-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a462c-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a462c-2017">Az.Media</span></span>
- <span data-ttu-id="a462c-2018">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="a462c-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a462c-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-2019">Az.Network</span></span>
<span data-ttu-id="a462c-2020">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a462c-2021">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="a462c-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a462c-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a462c-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a462c-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a462c-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a462c-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a462c-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a462c-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a462c-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a462c-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a462c-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a462c-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a462c-2030">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a462c-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a462c-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a462c-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a462c-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a462c-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a462c-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a462c-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a462c-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a462c-2036">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a462c-2037">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a462c-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a462c-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a462c-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a462c-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a462c-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a462c-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a462c-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a462c-2041">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a462c-2042">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a462c-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="a462c-2044">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a462c-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a462c-2045">Az.Profile</span></span>
- <span data-ttu-id="a462c-2046">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="a462c-2048">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a462c-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-2049">Az.Resources</span></span>
- <span data-ttu-id="a462c-2050">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a462c-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="a462c-2052">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="a462c-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a462c-2053">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a462c-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a462c-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="a462c-2055">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a462c-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a462c-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-2056">Az.Sql</span></span>
- <span data-ttu-id="a462c-2057">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a462c-2058">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a462c-2059">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a462c-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-2060">Az.Storage</span></span>
- <span data-ttu-id="a462c-2061">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a462c-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-2062">Az.Websites</span></span>
- <span data-ttu-id="a462c-2063">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a462c-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a462c-2064">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a462c-2065">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-2065">General</span></span>

* <span data-ttu-id="a462c-2066">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="a462c-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a462c-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-2067">Az.Compute</span></span>

* <span data-ttu-id="a462c-2068">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a462c-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="a462c-2070">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a462c-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a462c-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="a462c-2072">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="a462c-2073">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a462c-2074">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a462c-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a462c-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="a462c-2076">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a462c-2077">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="a462c-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a462c-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-2078">Az.Resources</span></span>

* <span data-ttu-id="a462c-2079">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a462c-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a462c-2080">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a462c-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a462c-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-2081">Az.Sql</span></span>

* <span data-ttu-id="a462c-2082">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="a462c-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a462c-2083">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a462c-2084">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="a462c-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a462c-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-2085">Az.Storage</span></span>

* <span data-ttu-id="a462c-2086">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a462c-2087">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="a462c-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a462c-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a462c-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a462c-2089">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="a462c-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a462c-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a462c-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a462c-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a462c-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-2092">Az.Websites</span></span>

* <span data-ttu-id="a462c-2093">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a462c-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="a462c-2094">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a462c-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a462c-2095">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="a462c-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a462c-2096">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a462c-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a462c-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="a462c-2098">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a462c-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a462c-2099">Az.Automation</span></span>
* <span data-ttu-id="a462c-2100">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a462c-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a462c-2101">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a462c-2102">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a462c-2103">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a462c-2104">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a462c-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-2105">Az.Compute</span></span>
* <span data-ttu-id="a462c-2106">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a462c-2107">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a462c-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="a462c-2109">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a462c-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a462c-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a462c-2111">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a462c-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-2112">Az.Network</span></span>
* <span data-ttu-id="a462c-2113">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a462c-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a462c-2114">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a462c-2115">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="a462c-2116">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a462c-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a462c-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a462c-2118">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a462c-2119">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="a462c-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a462c-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a462c-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a462c-2121">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="a462c-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a462c-2122">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a462c-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a462c-2123">Az.Relay</span></span>
* <span data-ttu-id="a462c-2124">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="a462c-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a462c-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-2125">Az.Resources</span></span>
* <span data-ttu-id="a462c-2126">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a462c-2127">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="a462c-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a462c-2128">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a462c-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a462c-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-2130">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a462c-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-2131">Az.Sql</span></span>
* <span data-ttu-id="a462c-2132">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a462c-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a462c-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a462c-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a462c-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a462c-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a462c-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a462c-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a462c-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a462c-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a462c-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a462c-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a462c-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a462c-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a462c-2141">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="a462c-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a462c-2142">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="a462c-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a462c-2143">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="a462c-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a462c-2144">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="a462c-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a462c-2145">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="a462c-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a462c-2146">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a462c-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a462c-2147">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a462c-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a462c-2148">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a462c-2149">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a462c-2150">Allgemein</span><span class="sxs-lookup"><span data-stu-id="a462c-2150">General</span></span>
* <span data-ttu-id="a462c-2151">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="a462c-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a462c-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a462c-2152">Az.Profile</span></span>
* <span data-ttu-id="a462c-2153">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a462c-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a462c-2154">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a462c-2155">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a462c-2156">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a462c-2157">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a462c-2158">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a462c-2159">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="a462c-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-2161">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-2162">Az.Compute</span></span>
* <span data-ttu-id="a462c-2163">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a462c-2164">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="a462c-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a462c-2165">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="a462c-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-2167">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="a462c-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a462c-2168">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a462c-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a462c-2169">Az.Insights</span></span>
* <span data-ttu-id="a462c-2170">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="a462c-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a462c-2171">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="a462c-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a462c-2172">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="a462c-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a462c-2173">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-2174">Az.Network</span></span>
* <span data-ttu-id="a462c-2175">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a462c-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a462c-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a462c-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a462c-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a462c-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a462c-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a462c-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a462c-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a462c-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a462c-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a462c-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a462c-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a462c-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a462c-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a462c-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="a462c-2183">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-2184">Az.Resources</span></span>
* <span data-ttu-id="a462c-2185">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a462c-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a462c-2186">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="a462c-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a462c-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a462c-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="a462c-2188">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="a462c-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a462c-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a462c-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="a462c-2190">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a462c-2191">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="a462c-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a462c-2192">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="a462c-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a462c-2193">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="a462c-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a462c-2194">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="a462c-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a462c-2195">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a462c-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a462c-2196">Az.Profile</span></span>
* <span data-ttu-id="a462c-2197">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a462c-2198">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a462c-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-2199">Az.Compute</span></span>
* <span data-ttu-id="a462c-2200">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="a462c-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a462c-2201">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a462c-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a462c-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="a462c-2203">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a462c-2204">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a462c-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a462c-2205">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="a462c-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a462c-2206">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="a462c-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a462c-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a462c-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-2208">Az.Network</span></span>
* <span data-ttu-id="a462c-2209">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="a462c-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a462c-2210">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-2211">Az.Resources</span></span>
* <span data-ttu-id="a462c-2212">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a462c-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a462c-2213">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a462c-2214">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a462c-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a462c-2215">Azure.Storage</span></span>
* <span data-ttu-id="a462c-2216">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="a462c-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a462c-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a462c-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a462c-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a462c-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a462c-2219">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="a462c-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a462c-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a462c-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a462c-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a462c-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="a462c-2222">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a462c-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a462c-2223">Az.Compute</span></span>
* <span data-ttu-id="a462c-2224">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="a462c-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a462c-2225">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a462c-2226">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="a462c-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a462c-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a462c-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a462c-2228">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a462c-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a462c-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a462c-2229">Az.Network</span></span>
* <span data-ttu-id="a462c-2230">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a462c-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a462c-2231">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2231">new cmdlets added</span></span>
    - <span data-ttu-id="a462c-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a462c-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a462c-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a462c-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a462c-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a462c-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a462c-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a462c-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a462c-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a462c-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a462c-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a462c-2238">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a462c-2239">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a462c-2240">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a462c-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a462c-2241">Az.RedisCache</span></span>
* <span data-ttu-id="a462c-2242">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="a462c-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a462c-2243">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a462c-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a462c-2244">Az.Resources</span></span>
* <span data-ttu-id="a462c-2245">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="a462c-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a462c-2246">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="a462c-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a462c-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a462c-2247">Az.Sql</span></span>
* <span data-ttu-id="a462c-2248">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="a462c-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a462c-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a462c-2249">Az.Websites</span></span>
* <span data-ttu-id="a462c-2250">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="a462c-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a462c-2251">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="a462c-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a462c-2252">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="a462c-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a462c-2253">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="a462c-2253">Initial Release</span></span>
