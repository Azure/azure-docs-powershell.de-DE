---
ms.openlocfilehash: e72aae940b48543d6a99801032186112748ea48b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657959"
---
## <a name="250---july-2019"></a><span data-ttu-id="045a0-101">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-102">Az.Accounts</span></span>
* <span data-ttu-id="045a0-103">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="045a0-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="045a0-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="045a0-105">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="045a0-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-106">Az.Automation</span></span>
* <span data-ttu-id="045a0-107">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="045a0-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="045a0-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="045a0-109">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-110">Az.Compute</span></span>
* <span data-ttu-id="045a0-111">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="045a0-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="045a0-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="045a0-113">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="045a0-114">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="045a0-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="045a0-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="045a0-115">Az.DataFactory</span></span>
* <span data-ttu-id="045a0-116">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="045a0-117">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="045a0-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="045a0-118">Az.EventHub</span></span>
* <span data-ttu-id="045a0-119">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="045a0-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="045a0-120">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="045a0-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="045a0-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="045a0-121">Az.KeyVault</span></span>
* <span data-ttu-id="045a0-122">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="045a0-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="045a0-123">Az.LogicApp</span></span>
* <span data-ttu-id="045a0-124">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="045a0-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="045a0-125">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="045a0-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="045a0-126">Az.ManagedServices</span></span>
* <span data-ttu-id="045a0-127">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-128">Az.Network</span></span>
* <span data-ttu-id="045a0-129">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="045a0-130">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-130">New cmdlets</span></span>
        - <span data-ttu-id="045a0-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="045a0-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="045a0-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="045a0-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="045a0-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="045a0-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="045a0-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="045a0-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="045a0-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="045a0-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="045a0-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="045a0-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="045a0-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="045a0-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="045a0-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="045a0-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="045a0-139">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="045a0-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="045a0-140">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="045a0-141">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, um anzugeben, dass durch Aktivierung oder Deaktivierung Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden</span><span class="sxs-lookup"><span data-stu-id="045a0-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="045a0-142">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, um anzugeben, dass durch Aktivierung oder Deaktivierung Netzwerkrichtlinien auf den privaten Verknüpfungsdienst in diesem Subnetz angewendet werden</span><span class="sxs-lookup"><span data-stu-id="045a0-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="045a0-143">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="045a0-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="045a0-144">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="045a0-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="045a0-145">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-145">Updated cmdlets</span></span>
        - <span data-ttu-id="045a0-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="045a0-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="045a0-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="045a0-149">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="045a0-150">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="045a0-151">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="045a0-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="045a0-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="045a0-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="045a0-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="045a0-155">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="045a0-156">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="045a0-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="045a0-157">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="045a0-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="045a0-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="045a0-159">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="045a0-160">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-162">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="045a0-163">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="045a0-164">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="045a0-165">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="045a0-166">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="045a0-167">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="045a0-168">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="045a0-169">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="045a0-170">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="045a0-171">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-172">Az.Resources</span></span>
- <span data-ttu-id="045a0-173">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="045a0-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="045a0-174">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="045a0-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="045a0-175">Az.ServiceBus</span></span>
* <span data-ttu-id="045a0-176">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="045a0-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="045a0-177">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="045a0-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-178">Az.Sql</span></span>
* <span data-ttu-id="045a0-179">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="045a0-180">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="045a0-181">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-182">Az.Storage</span></span>
* <span data-ttu-id="045a0-183">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="045a0-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="045a0-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="045a0-184">Az.StorageSync</span></span>
* <span data-ttu-id="045a0-185">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="045a0-186">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-187">Az.Websites</span></span>
* <span data-ttu-id="045a0-188">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="045a0-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="045a0-189">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="045a0-190">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="045a0-191">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-192">Az.Accounts</span></span>
* <span data-ttu-id="045a0-193">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="045a0-194">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="045a0-195">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="045a0-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="045a0-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="045a0-196">Az.Advisor</span></span>
* <span data-ttu-id="045a0-197">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="045a0-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="045a0-198">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="045a0-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="045a0-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="045a0-199">Az.ApiManagement</span></span>
* <span data-ttu-id="045a0-200">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="045a0-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="045a0-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="045a0-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="045a0-202">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="045a0-203">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="045a0-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="045a0-204">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="045a0-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="045a0-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="045a0-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="045a0-206">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-207">Az.Automation</span></span>
* <span data-ttu-id="045a0-208">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-209">Az.Compute</span></span>
* <span data-ttu-id="045a0-210">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="045a0-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="045a0-211">Az.DataFactory</span></span>
* <span data-ttu-id="045a0-212">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="045a0-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="045a0-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="045a0-213">Az.EventGrid</span></span>
* <span data-ttu-id="045a0-214">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="045a0-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="045a0-215">Az.IotHub</span></span>
* <span data-ttu-id="045a0-216">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-217">Az.Network</span></span>
* <span data-ttu-id="045a0-218">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="045a0-219">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="045a0-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="045a0-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="045a0-221">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="045a0-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="045a0-222">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="045a0-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="045a0-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="045a0-224">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-226">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="045a0-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-227">Az.Resources</span></span>
    - <span data-ttu-id="045a0-228">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="045a0-229">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="045a0-230">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="045a0-231">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="045a0-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="045a0-232">Az.ServiceBus</span></span>
* <span data-ttu-id="045a0-233">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="045a0-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-234">Az.Sql</span></span>
* <span data-ttu-id="045a0-235">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="045a0-236">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="045a0-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="045a0-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="045a0-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="045a0-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="045a0-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="045a0-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="045a0-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="045a0-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="045a0-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="045a0-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="045a0-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="045a0-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="045a0-243">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-244">Az.Storage</span></span>
* <span data-ttu-id="045a0-245">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="045a0-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="045a0-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="045a0-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="045a0-247">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="045a0-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="045a0-248">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="045a0-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="045a0-249">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="045a0-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="045a0-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="045a0-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="045a0-252">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="045a0-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="045a0-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="045a0-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="045a0-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="045a0-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="045a0-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="045a0-255">Az.StorageSync</span></span>
* <span data-ttu-id="045a0-256">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="045a0-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="045a0-257">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-258">Az.Accounts</span></span>
* <span data-ttu-id="045a0-259">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="045a0-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="045a0-260">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="045a0-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="045a0-261">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="045a0-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="045a0-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="045a0-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="045a0-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-264">Az.Compute</span></span>
* <span data-ttu-id="045a0-265">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="045a0-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="045a0-266">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="045a0-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="045a0-267">Az.Dns</span></span>
* <span data-ttu-id="045a0-268">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="045a0-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="045a0-269">Az.EventGrid</span></span>
* <span data-ttu-id="045a0-270">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="045a0-271">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="045a0-271">New cmdlets:</span></span>
    - <span data-ttu-id="045a0-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="045a0-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="045a0-273">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="045a0-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="045a0-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="045a0-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="045a0-275">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="045a0-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="045a0-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="045a0-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="045a0-277">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="045a0-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="045a0-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="045a0-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="045a0-279">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="045a0-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="045a0-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="045a0-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="045a0-281">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="045a0-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="045a0-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="045a0-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="045a0-283">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="045a0-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="045a0-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="045a0-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="045a0-285">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="045a0-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="045a0-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="045a0-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="045a0-287">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="045a0-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="045a0-288">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="045a0-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="045a0-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="045a0-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="045a0-290">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="045a0-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="045a0-291">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="045a0-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="045a0-292">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="045a0-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="045a0-293">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="045a0-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="045a0-294">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="045a0-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="045a0-295">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="045a0-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="045a0-296">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="045a0-297">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="045a0-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="045a0-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="045a0-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="045a0-299">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="045a0-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="045a0-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="045a0-301">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="045a0-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="045a0-302">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="045a0-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="045a0-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="045a0-303">Az.FrontDoor</span></span>
* <span data-ttu-id="045a0-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="045a0-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="045a0-305">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="045a0-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="045a0-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="045a0-307">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-308">Az.Network</span></span>
* <span data-ttu-id="045a0-309">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="045a0-310">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-310">New cmdlets</span></span>
        - <span data-ttu-id="045a0-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="045a0-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="045a0-312">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="045a0-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="045a0-313">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-313">New cmdlets</span></span> 
        - <span data-ttu-id="045a0-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="045a0-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="045a0-315">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="045a0-316">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-316">New cmdlets</span></span> 
        - <span data-ttu-id="045a0-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="045a0-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="045a0-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="045a0-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="045a0-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="045a0-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="045a0-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="045a0-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="045a0-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="045a0-322">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="045a0-323">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-323">New cmdlets</span></span>
        - <span data-ttu-id="045a0-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="045a0-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="045a0-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="045a0-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="045a0-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="045a0-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="045a0-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="045a0-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="045a0-328">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="045a0-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="045a0-329">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="045a0-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="045a0-330">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="045a0-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="045a0-331">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="045a0-332">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="045a0-333">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="045a0-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="045a0-334">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="045a0-335">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="045a0-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="045a0-336">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="045a0-337">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="045a0-338">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="045a0-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="045a0-339">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="045a0-340">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="045a0-341">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="045a0-342">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="045a0-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="045a0-343">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="045a0-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="045a0-344">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="045a0-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="045a0-345">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="045a0-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="045a0-346">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="045a0-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="045a0-347">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="045a0-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="045a0-348">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="045a0-349">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="045a0-350">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="045a0-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="045a0-352">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="045a0-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-353">Az.Resources</span></span>
* <span data-ttu-id="045a0-354">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="045a0-355">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="045a0-356">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="045a0-357">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="045a0-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="045a0-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="045a0-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="045a0-359">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="045a0-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-360">Az.Sql</span></span>
* <span data-ttu-id="045a0-361">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="045a0-362">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="045a0-363">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="045a0-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="045a0-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="045a0-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="045a0-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="045a0-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="045a0-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="045a0-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="045a0-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="045a0-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="045a0-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="045a0-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-369">Az.Storage</span></span>
* <span data-ttu-id="045a0-370">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="045a0-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="045a0-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="045a0-372">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="045a0-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="045a0-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="045a0-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-374">Az.Websites</span></span>
* <span data-ttu-id="045a0-375">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="045a0-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="045a0-376">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="045a0-377">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="045a0-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="045a0-378">Az.Cdn</span></span>
* <span data-ttu-id="045a0-379">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="045a0-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-380">Az.Compute</span></span>
* <span data-ttu-id="045a0-381">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="045a0-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="045a0-382">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="045a0-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="045a0-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="045a0-383">Az.EventHub</span></span>
* <span data-ttu-id="045a0-384">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="045a0-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="045a0-385">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="045a0-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-386">Az.Network</span></span>
* <span data-ttu-id="045a0-387">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="045a0-388">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="045a0-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="045a0-390">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="045a0-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-392">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="045a0-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="045a0-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="045a0-393">Az.ServiceBus</span></span>
* <span data-ttu-id="045a0-394">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="045a0-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="045a0-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="045a0-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="045a0-396">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="045a0-397">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-398">Az.Sql</span></span>
* <span data-ttu-id="045a0-399">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="045a0-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="045a0-400">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="045a0-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="045a0-401">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="045a0-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="045a0-402">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="045a0-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-403">Az.Websites</span></span>
* <span data-ttu-id="045a0-404">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="045a0-405">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="045a0-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="045a0-406">Az.ApiManagement</span></span>
* <span data-ttu-id="045a0-407">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="045a0-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="045a0-408">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="045a0-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="045a0-409">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="045a0-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="045a0-410">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="045a0-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="045a0-411">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="045a0-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="045a0-412">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="045a0-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="045a0-413">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="045a0-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="045a0-414">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="045a0-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="045a0-415">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="045a0-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="045a0-416">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="045a0-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="045a0-417">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="045a0-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="045a0-418">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="045a0-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="045a0-419">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="045a0-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="045a0-420">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="045a0-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="045a0-421">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="045a0-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="045a0-422">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="045a0-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="045a0-423">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="045a0-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="045a0-424">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="045a0-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="045a0-425">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="045a0-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="045a0-426">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="045a0-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="045a0-427">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="045a0-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="045a0-428">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="045a0-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="045a0-429">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="045a0-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="045a0-430">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="045a0-431">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="045a0-432">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="045a0-433">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="045a0-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="045a0-434">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="045a0-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="045a0-435">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="045a0-436">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="045a0-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="045a0-437">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="045a0-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="045a0-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="045a0-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="045a0-439">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="045a0-440">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="045a0-441">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="045a0-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="045a0-442">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="045a0-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="045a0-443">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="045a0-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="045a0-444">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="045a0-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="045a0-445">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="045a0-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="045a0-446">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="045a0-447">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="045a0-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="045a0-448">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="045a0-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="045a0-449">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="045a0-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="045a0-450">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="045a0-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="045a0-451">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="045a0-452">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="045a0-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="045a0-453">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="045a0-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="045a0-454">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="045a0-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="045a0-455">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="045a0-456">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="045a0-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="045a0-457">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="045a0-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="045a0-458">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="045a0-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="045a0-459">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="045a0-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="045a0-460">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="045a0-461">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="045a0-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="045a0-462">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="045a0-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="045a0-463">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="045a0-464">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="045a0-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="045a0-465">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="045a0-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="045a0-466">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="045a0-467">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="045a0-468">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="045a0-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="045a0-469">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="045a0-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="045a0-470">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="045a0-471">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="045a0-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="045a0-472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="045a0-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="045a0-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="045a0-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="045a0-474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="045a0-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="045a0-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="045a0-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="045a0-476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="045a0-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="045a0-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="045a0-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="045a0-478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="045a0-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="045a0-479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="045a0-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="045a0-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="045a0-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="045a0-481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="045a0-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="045a0-482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="045a0-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="045a0-483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="045a0-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-484">Az.Automation</span></span>
* <span data-ttu-id="045a0-485">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="045a0-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="045a0-486">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="045a0-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="045a0-487">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="045a0-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="045a0-488">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="045a0-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="045a0-489">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="045a0-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="045a0-490">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="045a0-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="045a0-491">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="045a0-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-492">Az.Compute</span></span>
* <span data-ttu-id="045a0-493">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="045a0-494">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="045a0-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-496">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="045a0-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="045a0-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="045a0-497">Az.Monitor</span></span>
* <span data-ttu-id="045a0-498">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="045a0-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-499">Az.Network</span></span>
* <span data-ttu-id="045a0-500">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="045a0-501">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="045a0-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="045a0-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="045a0-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="045a0-503">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="045a0-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-504">Az.Resources</span></span>
* <span data-ttu-id="045a0-505">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-506">Az.Sql</span></span>
* <span data-ttu-id="045a0-507">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="045a0-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="045a0-508">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-509">Az.Accounts</span></span>
* <span data-ttu-id="045a0-510">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="045a0-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="045a0-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="045a0-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="045a0-512">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="045a0-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="045a0-513">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="045a0-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-514">Az.Compute</span></span>
* <span data-ttu-id="045a0-515">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="045a0-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="045a0-516">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="045a0-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="045a0-517">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="045a0-518">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="045a0-519">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="045a0-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="045a0-520">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="045a0-521">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="045a0-521">Breaking changes</span></span>
    - <span data-ttu-id="045a0-522">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="045a0-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="045a0-523">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="045a0-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="045a0-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="045a0-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="045a0-525">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="045a0-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="045a0-526">Az.Dns</span></span>
* <span data-ttu-id="045a0-527">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="045a0-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="045a0-528">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="045a0-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="045a0-529">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="045a0-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="045a0-530">Az.FrontDoor</span></span>
* <span data-ttu-id="045a0-531">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="045a0-532">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="045a0-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="045a0-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="045a0-533">Az.HDInsight</span></span>
* <span data-ttu-id="045a0-534">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="045a0-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="045a0-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="045a0-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="045a0-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="045a0-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="045a0-537">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="045a0-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="045a0-538">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="045a0-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="045a0-539">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="045a0-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="045a0-540">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="045a0-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="045a0-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="045a0-541">Az.Monitor</span></span>
* <span data-ttu-id="045a0-542">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="045a0-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="045a0-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="045a0-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="045a0-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="045a0-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="045a0-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="045a0-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="045a0-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="045a0-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="045a0-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="045a0-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="045a0-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="045a0-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="045a0-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="045a0-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="045a0-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="045a0-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="045a0-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="045a0-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="045a0-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="045a0-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="045a0-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="045a0-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="045a0-554">[Weitere Informationen](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="045a0-554">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="045a0-555">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="045a0-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-556">Az.Network</span></span>
* <span data-ttu-id="045a0-557">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="045a0-558">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-558">New cmdlets</span></span>
        - <span data-ttu-id="045a0-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="045a0-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="045a0-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="045a0-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="045a0-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="045a0-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="045a0-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="045a0-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="045a0-563">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-563">Updated cmdlets</span></span>
        - <span data-ttu-id="045a0-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="045a0-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="045a0-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="045a0-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="045a0-566">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="045a0-567">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="045a0-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="045a0-568">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="045a0-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="045a0-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="045a0-570">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="045a0-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="045a0-571">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="045a0-572">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="045a0-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-574">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="045a0-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="045a0-575">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="045a0-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="045a0-576">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="045a0-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="045a0-577">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="045a0-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="045a0-578">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="045a0-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="045a0-579">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="045a0-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="045a0-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="045a0-580">Az.Relay</span></span>
* <span data-ttu-id="045a0-581">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="045a0-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="045a0-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="045a0-582">Az.ServiceBus</span></span>
* <span data-ttu-id="045a0-583">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-584">Az.Storage</span></span>
* <span data-ttu-id="045a0-585">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="045a0-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="045a0-586">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="045a0-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="045a0-587">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="045a0-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="045a0-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="045a0-589">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="045a0-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="045a0-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="045a0-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="045a0-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-593">Az.Websites</span></span>
* <span data-ttu-id="045a0-594">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="045a0-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="045a0-595">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="045a0-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="045a0-596">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="045a0-597">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="045a0-597">Highlights since the last major release</span></span>
* <span data-ttu-id="045a0-598">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="045a0-598">General availability of `Az` module</span></span>
* <span data-ttu-id="045a0-599">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="045a0-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="045a0-600">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="045a0-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="045a0-601">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="045a0-602">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="045a0-603">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="045a0-604">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="045a0-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-605">Az.Accounts</span></span>
* <span data-ttu-id="045a0-606">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="045a0-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="045a0-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="045a0-607">Az.Batch</span></span>
* <span data-ttu-id="045a0-608">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="045a0-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="045a0-609">Az.Cdn</span></span>
* <span data-ttu-id="045a0-610">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="045a0-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="045a0-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="045a0-612">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-613">Az.Compute</span></span>
* <span data-ttu-id="045a0-614">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="045a0-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="045a0-615">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="045a0-616">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="045a0-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="045a0-617">Az.DataFactory</span></span>
* <span data-ttu-id="045a0-618">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="045a0-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-620">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="045a0-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="045a0-621">Az.EventGrid</span></span>
* <span data-ttu-id="045a0-622">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="045a0-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="045a0-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="045a0-623">Az.EventHub</span></span>
* <span data-ttu-id="045a0-624">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="045a0-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="045a0-625">Az.HDInsight</span></span>
* <span data-ttu-id="045a0-626">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="045a0-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="045a0-627">Az.IotHub</span></span>
* <span data-ttu-id="045a0-628">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="045a0-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="045a0-629">Az.KeyVault</span></span>
* <span data-ttu-id="045a0-630">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="045a0-631">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="045a0-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="045a0-632">Az.MachineLearning</span></span>
* <span data-ttu-id="045a0-633">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="045a0-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="045a0-634">Az.Media</span></span>
* <span data-ttu-id="045a0-635">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="045a0-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="045a0-636">Az.Monitor</span></span>
  * <span data-ttu-id="045a0-637">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="045a0-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="045a0-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="045a0-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="045a0-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="045a0-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="045a0-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="045a0-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="045a0-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="045a0-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="045a0-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="045a0-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="045a0-643">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-644">Az.Network</span></span>
* <span data-ttu-id="045a0-645">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="045a0-646">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="045a0-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="045a0-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="045a0-648">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="045a0-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="045a0-650">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="045a0-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="045a0-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="045a0-652">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-654">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="045a0-655">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="045a0-656">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="045a0-657">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="045a0-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="045a0-658">Az.RedisCache</span></span>
* <span data-ttu-id="045a0-659">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-660">Az.Resources</span></span>
* <span data-ttu-id="045a0-661">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-662">Az.Sql</span></span>
* <span data-ttu-id="045a0-663">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="045a0-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="045a0-664">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="045a0-665">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="045a0-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="045a0-666">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="045a0-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="045a0-667">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="045a0-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="045a0-668">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="045a0-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="045a0-669">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-670">Az.Websites</span></span>
* <span data-ttu-id="045a0-671">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="045a0-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="045a0-672">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="045a0-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="045a0-673">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="045a0-674">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="045a0-675">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="045a0-676">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="045a0-676">Highlights since the last major release</span></span>
* <span data-ttu-id="045a0-677">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="045a0-677">General availability of `Az` module</span></span>
* <span data-ttu-id="045a0-678">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="045a0-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="045a0-679">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="045a0-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="045a0-680">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="045a0-681">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="045a0-682">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="045a0-683">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="045a0-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-684">Az.Accounts</span></span>
* <span data-ttu-id="045a0-685">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="045a0-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="045a0-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="045a0-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="045a0-687">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="045a0-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="045a0-688">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="045a0-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-689">Az.Automation</span></span>
* <span data-ttu-id="045a0-690">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="045a0-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="045a0-691">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="045a0-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="045a0-692">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="045a0-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-693">Az.Compute</span></span>
* <span data-ttu-id="045a0-694">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="045a0-695">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="045a0-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="045a0-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="045a0-697">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="045a0-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="045a0-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="045a0-698">Az.DataFactory</span></span>
* <span data-ttu-id="045a0-699">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="045a0-700">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-701">Az.Resources</span></span>
* <span data-ttu-id="045a0-702">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="045a0-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="045a0-703">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="045a0-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="045a0-704">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="045a0-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="045a0-705">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="045a0-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="045a0-706">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="045a0-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="045a0-707">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="045a0-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-708">Az.Sql</span></span>
* <span data-ttu-id="045a0-709">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="045a0-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-710">Az.Storage</span></span>
* <span data-ttu-id="045a0-711">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="045a0-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="045a0-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="045a0-712">New-AzStorageContext</span></span>
* <span data-ttu-id="045a0-713">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="045a0-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="045a0-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="045a0-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="045a0-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="045a0-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="045a0-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="045a0-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="045a0-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="045a0-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="045a0-718">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="045a0-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="045a0-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="045a0-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="045a0-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="045a0-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="045a0-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="045a0-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="045a0-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="045a0-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="045a0-723">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="045a0-724">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="045a0-724">Highlights since the last major release</span></span>
* <span data-ttu-id="045a0-725">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="045a0-725">General availability of `Az` module</span></span>
* <span data-ttu-id="045a0-726">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="045a0-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="045a0-727">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="045a0-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="045a0-728">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="045a0-729">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="045a0-730">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="045a0-731">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-732">Az.Automation</span></span>
* <span data-ttu-id="045a0-733">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="045a0-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="045a0-734">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="045a0-734">Dynamic grouping</span></span>
    * <span data-ttu-id="045a0-735">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="045a0-735">Pre-Post script</span></span>
    * <span data-ttu-id="045a0-736">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="045a0-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-737">Az.Compute</span></span>
* <span data-ttu-id="045a0-738">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="045a0-739">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="045a0-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="045a0-740">Az.KeyVault</span></span>
* <span data-ttu-id="045a0-741">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-742">Az.Network</span></span>
* <span data-ttu-id="045a0-743">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="045a0-744">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-746">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="045a0-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="045a0-747">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-748">Az.Resources</span></span>
* <span data-ttu-id="045a0-749">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="045a0-750">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="045a0-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-751">Az.Sql</span></span>
* <span data-ttu-id="045a0-752">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="045a0-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-753">Az.Storage</span></span>
* <span data-ttu-id="045a0-754">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="045a0-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="045a0-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="045a0-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="045a0-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="045a0-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="045a0-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="045a0-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="045a0-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="045a0-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="045a0-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="045a0-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="045a0-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-761">Az.Websites</span></span>
* <span data-ttu-id="045a0-762">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="045a0-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="045a0-763">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-764">Az.Accounts</span></span>
* <span data-ttu-id="045a0-765">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="045a0-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="045a0-766">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-767">Az.Automation</span></span>
* <span data-ttu-id="045a0-768">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="045a0-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="045a0-769">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="045a0-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="045a0-770">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="045a0-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="045a0-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="045a0-771">Az.Cdn</span></span>
* <span data-ttu-id="045a0-772">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="045a0-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-773">Az.Compute</span></span>
* <span data-ttu-id="045a0-774">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="045a0-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="045a0-775">Az.DataFactory</span></span>
* <span data-ttu-id="045a0-776">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="045a0-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="045a0-777">Az.LogicApp</span></span>
* <span data-ttu-id="045a0-778">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="045a0-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-779">Az.Network</span></span>
* <span data-ttu-id="045a0-780">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-782">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="045a0-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="045a0-783">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="045a0-783">SDK Update</span></span>
* <span data-ttu-id="045a0-784">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="045a0-785">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-786">Az.Resources</span></span>
* <span data-ttu-id="045a0-787">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="045a0-788">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="045a0-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="045a0-789">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="045a0-790">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="045a0-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="045a0-791">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="045a0-792">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="045a0-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-793">Az.Sql</span></span>
* <span data-ttu-id="045a0-794">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="045a0-795">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-796">Az.Storage</span></span>
* <span data-ttu-id="045a0-797">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="045a0-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="045a0-798">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="045a0-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="045a0-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="045a0-800">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="045a0-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-801">Az.Automation</span></span>
* <span data-ttu-id="045a0-802">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="045a0-803">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="045a0-804">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="045a0-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="045a0-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="045a0-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="045a0-806">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="045a0-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-807">Az.Compute</span></span>
* <span data-ttu-id="045a0-808">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="045a0-809">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="045a0-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="045a0-810">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="045a0-811">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="045a0-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-813">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="045a0-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="045a0-814">Az.EventHub</span></span>
* <span data-ttu-id="045a0-815">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="045a0-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="045a0-816">Az.KeyVault</span></span>
* <span data-ttu-id="045a0-817">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="045a0-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="045a0-818">Az.LogicApp</span></span>
* <span data-ttu-id="045a0-819">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="045a0-820">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="045a0-821">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="045a0-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="045a0-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="045a0-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="045a0-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="045a0-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="045a0-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="045a0-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="045a0-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="045a0-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="045a0-826">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="045a0-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="045a0-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="045a0-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="045a0-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="045a0-831">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="045a0-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="045a0-832">Az.Monitor</span></span>
* <span data-ttu-id="045a0-833">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-834">Az.Network</span></span>
* <span data-ttu-id="045a0-835">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="045a0-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="045a0-837">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="045a0-838">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="045a0-839">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="045a0-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="045a0-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-840">Az.Resources</span></span>
* <span data-ttu-id="045a0-841">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="045a0-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="045a0-842">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="045a0-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="045a0-843">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="045a0-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="045a0-844">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="045a0-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-845">Az.Sql</span></span>
* <span data-ttu-id="045a0-846">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="045a0-847">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="045a0-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-848">Az.Websites</span></span>
* <span data-ttu-id="045a0-849">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="045a0-850">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-851">Az.Accounts</span></span>
* <span data-ttu-id="045a0-852">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="045a0-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="045a0-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="045a0-853">Az.AnalysisServices</span></span>
<span data-ttu-id="045a0-854">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="045a0-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-855">Az.Compute</span></span>
* <span data-ttu-id="045a0-856">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="045a0-857">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="045a0-858">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-859">Az.RecoveryServices</span></span>
<span data-ttu-id="045a0-860">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="045a0-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-861">Az.Resources</span></span>
* <span data-ttu-id="045a0-862">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="045a0-863">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="045a0-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="045a0-864">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="045a0-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="045a0-865">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="045a0-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-866">Az.Sql</span></span>
* <span data-ttu-id="045a0-867">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="045a0-868">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="045a0-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="045a0-869">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="045a0-870">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-871">Az.Accounts</span></span>
* <span data-ttu-id="045a0-872">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="045a0-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="045a0-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="045a0-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="045a0-874">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="045a0-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="045a0-876">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="045a0-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="045a0-877">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-878">Az.Accounts</span></span>
* <span data-ttu-id="045a0-879">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="045a0-880">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="045a0-881">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="045a0-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="045a0-882">Az.Aks</span></span>
* <span data-ttu-id="045a0-883">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="045a0-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-884">Az.Automation</span></span>
* <span data-ttu-id="045a0-885">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="045a0-886">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="045a0-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="045a0-887">Az.Cdn</span></span>
* <span data-ttu-id="045a0-888">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-889">Az.Compute</span></span>
* <span data-ttu-id="045a0-890">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="045a0-891">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="045a0-892">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="045a0-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="045a0-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="045a0-894">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="045a0-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="045a0-895">Az.DataFactory</span></span>
* <span data-ttu-id="045a0-896">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-898">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="045a0-899">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="045a0-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="045a0-900">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="045a0-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="045a0-901">Az.IotHub</span></span>
* <span data-ttu-id="045a0-902">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="045a0-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="045a0-903">Az.KeyVault</span></span>
* <span data-ttu-id="045a0-904">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-905">Az.Network</span></span>
* <span data-ttu-id="045a0-906">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-907">Az.Resources</span></span>
* <span data-ttu-id="045a0-908">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="045a0-909">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="045a0-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="045a0-910">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="045a0-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="045a0-911">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="045a0-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="045a0-912">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="045a0-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="045a0-913">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="045a0-914">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="045a0-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="045a0-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="045a0-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="045a0-916">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="045a0-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="045a0-917">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-917">Fix some error messages.</span></span>
* <span data-ttu-id="045a0-918">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="045a0-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="045a0-919">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="045a0-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="045a0-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="045a0-920">Az.SignalR</span></span>
* <span data-ttu-id="045a0-921">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-922">Az.Sql</span></span>
* <span data-ttu-id="045a0-923">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="045a0-924">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="045a0-925">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="045a0-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="045a0-926">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="045a0-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-927">Az.Storage</span></span>
* <span data-ttu-id="045a0-928">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="045a0-929">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="045a0-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="045a0-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="045a0-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="045a0-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="045a0-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="045a0-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="045a0-932">Az.TrafficManager</span></span>
* <span data-ttu-id="045a0-933">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-934">Az.Websites</span></span>
* <span data-ttu-id="045a0-935">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="045a0-936">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="045a0-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="045a0-937">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="045a0-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="045a0-938">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="045a0-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="045a0-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-939">Az.Accounts</span></span>
* <span data-ttu-id="045a0-940">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-941">Az.Compute</span></span>
* <span data-ttu-id="045a0-942">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="045a0-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="045a0-943">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="045a0-944">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-946">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="045a0-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="045a0-947">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="045a0-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="045a0-948">Az.EventGrid</span></span>
* <span data-ttu-id="045a0-949">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="045a0-950">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="045a0-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="045a0-951">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="045a0-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="045a0-952">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="045a0-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="045a0-953">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="045a0-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="045a0-954">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="045a0-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="045a0-955">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="045a0-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="045a0-956">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="045a0-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="045a0-957">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="045a0-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="045a0-958">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="045a0-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="045a0-959">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="045a0-960">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="045a0-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="045a0-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="045a0-961">Az.IotHub</span></span>
* <span data-ttu-id="045a0-962">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="045a0-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="045a0-963">Az.LogicApp</span></span>
* <span data-ttu-id="045a0-964">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="045a0-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-965">Az.Resources</span></span>
* <span data-ttu-id="045a0-966">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="045a0-967">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="045a0-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="045a0-968">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="045a0-969">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="045a0-970">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="045a0-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="045a0-971">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="045a0-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="045a0-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="045a0-972">Az.SignalR</span></span>
* <span data-ttu-id="045a0-973">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-974">Az.Sql</span></span>
* <span data-ttu-id="045a0-975">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="045a0-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="045a0-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-976">Az.Storage</span></span>
* <span data-ttu-id="045a0-977">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="045a0-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="045a0-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="045a0-978">New-AzStorageContext</span></span>
* <span data-ttu-id="045a0-979">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="045a0-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="045a0-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="045a0-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-981">Az.Websites</span></span>
* <span data-ttu-id="045a0-982">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="045a0-983">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="045a0-984">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="045a0-985">Allgemein</span><span class="sxs-lookup"><span data-stu-id="045a0-985">General</span></span>

- <span data-ttu-id="045a0-986">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="045a0-986">General Availability of Az Module</span></span>
- <span data-ttu-id="045a0-987">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="045a0-987">Online help for each module</span></span>
- <span data-ttu-id="045a0-988">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="045a0-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="045a0-989">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="045a0-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="045a0-990">Az.Accounts</span></span>
- <span data-ttu-id="045a0-991">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="045a0-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="045a0-992">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="045a0-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="045a0-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="045a0-993">Az.ApiManagement</span></span>
- <span data-ttu-id="045a0-994">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="045a0-994">Fixes for #7002</span></span>
- <span data-ttu-id="045a0-995">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="045a0-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="045a0-996">Az.Batch</span></span>
- <span data-ttu-id="045a0-997">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="045a0-998">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="045a0-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="045a0-999">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="045a0-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="045a0-1000">Az.Billing</span></span>
- <span data-ttu-id="045a0-1001">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="045a0-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="045a0-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="045a0-1003">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="045a0-1004">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="045a0-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="045a0-1006">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="045a0-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="045a0-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="045a0-1008">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="045a0-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="045a0-1010">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="045a0-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="045a0-1011">Az.Monitor</span></span>
- <span data-ttu-id="045a0-1012">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="045a0-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="045a0-1013">Az.KeyVault</span></span>
- <span data-ttu-id="045a0-1014">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="045a0-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="045a0-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="045a0-1016">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="045a0-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="045a0-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="045a0-1017">Az.Media</span></span>
- <span data-ttu-id="045a0-1018">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="045a0-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="045a0-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-1019">Az.Network</span></span>
<span data-ttu-id="045a0-1020">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="045a0-1021">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="045a0-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="045a0-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="045a0-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="045a0-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="045a0-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="045a0-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="045a0-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="045a0-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="045a0-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="045a0-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="045a0-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="045a0-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="045a0-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="045a0-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="045a0-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="045a0-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="045a0-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="045a0-1030">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="045a0-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="045a0-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="045a0-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="045a0-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="045a0-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="045a0-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="045a0-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="045a0-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="045a0-1036">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="045a0-1037">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="045a0-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="045a0-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="045a0-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="045a0-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="045a0-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="045a0-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="045a0-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="045a0-1041">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="045a0-1042">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="045a0-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="045a0-1044">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="045a0-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="045a0-1045">Az.Profile</span></span>
- <span data-ttu-id="045a0-1046">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="045a0-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="045a0-1048">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="045a0-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-1049">Az.Resources</span></span>
- <span data-ttu-id="045a0-1050">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="045a0-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="045a0-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="045a0-1052">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="045a0-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="045a0-1053">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="045a0-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="045a0-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="045a0-1055">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="045a0-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="045a0-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-1056">Az.Sql</span></span>
- <span data-ttu-id="045a0-1057">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="045a0-1058">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="045a0-1059">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="045a0-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-1060">Az.Storage</span></span>
- <span data-ttu-id="045a0-1061">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="045a0-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-1062">Az.Websites</span></span>
- <span data-ttu-id="045a0-1063">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="045a0-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="045a0-1064">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="045a0-1065">Allgemein</span><span class="sxs-lookup"><span data-stu-id="045a0-1065">General</span></span>

* <span data-ttu-id="045a0-1066">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="045a0-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="045a0-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-1067">Az.Compute</span></span>

* <span data-ttu-id="045a0-1068">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="045a0-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="045a0-1070">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="045a0-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="045a0-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="045a0-1072">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="045a0-1073">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="045a0-1074">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="045a0-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="045a0-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="045a0-1076">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="045a0-1077">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="045a0-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="045a0-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-1078">Az.Resources</span></span>

* <span data-ttu-id="045a0-1079">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="045a0-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="045a0-1080">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="045a0-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="045a0-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-1081">Az.Sql</span></span>

* <span data-ttu-id="045a0-1082">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="045a0-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="045a0-1083">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="045a0-1084">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="045a0-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="045a0-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-1085">Az.Storage</span></span>

* <span data-ttu-id="045a0-1086">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="045a0-1087">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="045a0-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="045a0-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="045a0-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="045a0-1089">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="045a0-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="045a0-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="045a0-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="045a0-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="045a0-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-1092">Az.Websites</span></span>

* <span data-ttu-id="045a0-1093">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="045a0-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="045a0-1094">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="045a0-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="045a0-1095">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="045a0-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="045a0-1096">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="045a0-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="045a0-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="045a0-1098">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="045a0-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="045a0-1099">Az.Automation</span></span>
* <span data-ttu-id="045a0-1100">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="045a0-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="045a0-1101">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="045a0-1102">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="045a0-1103">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="045a0-1104">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="045a0-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-1105">Az.Compute</span></span>
* <span data-ttu-id="045a0-1106">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="045a0-1107">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="045a0-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="045a0-1109">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="045a0-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="045a0-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="045a0-1111">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="045a0-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-1112">Az.Network</span></span>
* <span data-ttu-id="045a0-1113">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="045a0-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="045a0-1114">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="045a0-1115">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="045a0-1116">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="045a0-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="045a0-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="045a0-1118">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="045a0-1119">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="045a0-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="045a0-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="045a0-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="045a0-1121">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="045a0-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="045a0-1122">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="045a0-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="045a0-1123">Az.Relay</span></span>
* <span data-ttu-id="045a0-1124">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="045a0-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="045a0-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-1125">Az.Resources</span></span>
* <span data-ttu-id="045a0-1126">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="045a0-1127">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="045a0-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="045a0-1128">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="045a0-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="045a0-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="045a0-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="045a0-1130">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="045a0-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-1131">Az.Sql</span></span>
* <span data-ttu-id="045a0-1132">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="045a0-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="045a0-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="045a0-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="045a0-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="045a0-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="045a0-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="045a0-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="045a0-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="045a0-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="045a0-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="045a0-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="045a0-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="045a0-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="045a0-1141">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="045a0-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="045a0-1142">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="045a0-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="045a0-1143">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="045a0-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="045a0-1144">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="045a0-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="045a0-1145">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="045a0-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="045a0-1146">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="045a0-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="045a0-1147">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="045a0-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="045a0-1148">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="045a0-1149">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="045a0-1150">Allgemein</span><span class="sxs-lookup"><span data-stu-id="045a0-1150">General</span></span>
* <span data-ttu-id="045a0-1151">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="045a0-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="045a0-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="045a0-1152">Az.Profile</span></span>
* <span data-ttu-id="045a0-1153">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="045a0-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="045a0-1154">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="045a0-1155">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="045a0-1156">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="045a0-1157">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="045a0-1158">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="045a0-1159">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="045a0-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="045a0-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="045a0-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="045a0-1161">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-1162">Az.Compute</span></span>
* <span data-ttu-id="045a0-1163">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="045a0-1164">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="045a0-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="045a0-1165">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="045a0-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-1167">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="045a0-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="045a0-1168">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="045a0-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="045a0-1169">Az.Insights</span></span>
* <span data-ttu-id="045a0-1170">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="045a0-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="045a0-1171">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="045a0-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="045a0-1172">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="045a0-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="045a0-1173">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-1174">Az.Network</span></span>
* <span data-ttu-id="045a0-1175">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="045a0-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="045a0-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="045a0-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="045a0-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="045a0-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="045a0-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="045a0-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="045a0-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="045a0-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="045a0-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="045a0-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="045a0-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="045a0-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="045a0-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="045a0-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="045a0-1183">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-1184">Az.Resources</span></span>
* <span data-ttu-id="045a0-1185">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="045a0-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="045a0-1186">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="045a0-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="045a0-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="045a0-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="045a0-1188">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="045a0-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="045a0-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="045a0-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="045a0-1190">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="045a0-1191">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="045a0-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="045a0-1192">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="045a0-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="045a0-1193">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="045a0-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="045a0-1194">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="045a0-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="045a0-1195">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="045a0-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="045a0-1196">Az.Profile</span></span>
* <span data-ttu-id="045a0-1197">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="045a0-1198">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="045a0-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-1199">Az.Compute</span></span>
* <span data-ttu-id="045a0-1200">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="045a0-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="045a0-1201">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="045a0-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="045a0-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="045a0-1203">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="045a0-1204">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="045a0-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="045a0-1205">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="045a0-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="045a0-1206">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="045a0-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="045a0-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="045a0-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-1208">Az.Network</span></span>
* <span data-ttu-id="045a0-1209">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="045a0-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="045a0-1210">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-1211">Az.Resources</span></span>
* <span data-ttu-id="045a0-1212">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="045a0-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="045a0-1213">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="045a0-1214">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="045a0-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="045a0-1215">Azure.Storage</span></span>
* <span data-ttu-id="045a0-1216">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="045a0-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="045a0-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="045a0-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="045a0-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="045a0-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="045a0-1219">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="045a0-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="045a0-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="045a0-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="045a0-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="045a0-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="045a0-1222">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="045a0-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="045a0-1223">Az.Compute</span></span>
* <span data-ttu-id="045a0-1224">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="045a0-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="045a0-1225">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="045a0-1226">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="045a0-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="045a0-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="045a0-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="045a0-1228">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="045a0-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="045a0-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="045a0-1229">Az.Network</span></span>
* <span data-ttu-id="045a0-1230">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="045a0-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="045a0-1231">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1231">new cmdlets added</span></span>
    - <span data-ttu-id="045a0-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="045a0-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="045a0-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="045a0-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="045a0-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="045a0-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="045a0-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="045a0-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="045a0-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="045a0-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="045a0-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="045a0-1238">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="045a0-1239">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="045a0-1240">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="045a0-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="045a0-1241">Az.RedisCache</span></span>
* <span data-ttu-id="045a0-1242">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="045a0-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="045a0-1243">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="045a0-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="045a0-1244">Az.Resources</span></span>
* <span data-ttu-id="045a0-1245">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="045a0-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="045a0-1246">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="045a0-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="045a0-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="045a0-1247">Az.Sql</span></span>
* <span data-ttu-id="045a0-1248">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="045a0-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="045a0-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="045a0-1249">Az.Websites</span></span>
* <span data-ttu-id="045a0-1250">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="045a0-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="045a0-1251">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="045a0-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="045a0-1252">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="045a0-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="045a0-1253">Erste Version</span><span class="sxs-lookup"><span data-stu-id="045a0-1253">Initial Release</span></span>