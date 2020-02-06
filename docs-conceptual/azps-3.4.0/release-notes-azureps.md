---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002672"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0699a-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0699a-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0699a-104">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="0699a-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0699a-105">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0699a-105">Highlights since the last major release</span></span>
* <span data-ttu-id="0699a-106">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="0699a-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0699a-107">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-108">Az.Accounts</span></span>
* <span data-ttu-id="0699a-109">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="0699a-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0699a-110">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="0699a-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0699a-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-111">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-112">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0699a-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0699a-113">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0699a-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0699a-114">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="0699a-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0699a-115">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="0699a-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-116">Az.Compute</span></span>
* <span data-ttu-id="0699a-117">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0699a-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0699a-118">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0699a-119">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0699a-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0699a-121">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-122">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-123">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0699a-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0699a-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="0699a-125">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0699a-126">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0699a-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0699a-127">Az.HDInsight</span></span>
* <span data-ttu-id="0699a-128">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-129">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-130">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="0699a-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-131">Az.Network</span></span>
* <span data-ttu-id="0699a-132">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="0699a-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0699a-133">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0699a-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0699a-134">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="0699a-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0699a-135">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="0699a-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0699a-136">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="0699a-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0699a-137">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="0699a-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0699a-138">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="0699a-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0699a-139">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0699a-140">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-140">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0699a-142">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0699a-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0699a-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0699a-144">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0699a-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="0699a-146">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0699a-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0699a-147">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0699a-148">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0699a-149">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-151">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="0699a-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0699a-152">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-153">Az.Resources</span></span>
* <span data-ttu-id="0699a-154">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="0699a-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0699a-155">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-156">Az.Sql</span></span>
<span data-ttu-id="0699a-157">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="0699a-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-158">Az.Storage</span></span>
* <span data-ttu-id="0699a-159">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0699a-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0699a-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="0699a-161">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="0699a-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0699a-162">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-163">Az.Websites</span></span>
* <span data-ttu-id="0699a-164">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="0699a-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0699a-165">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="0699a-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0699a-166">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="0699a-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-167">Az.Accounts</span></span>
* <span data-ttu-id="0699a-168">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="0699a-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0699a-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-169">Az.Cdn</span></span>
* <span data-ttu-id="0699a-170">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="0699a-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-171">Az.Compute</span></span>
* <span data-ttu-id="0699a-172">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0699a-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="0699a-174">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0699a-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0699a-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0699a-176">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0699a-177">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="0699a-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0699a-178">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0699a-179">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="0699a-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0699a-180">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0699a-181">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="0699a-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0699a-182">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0699a-183">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="0699a-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0699a-184">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0699a-185">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="0699a-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0699a-186">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0699a-187">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="0699a-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0699a-188">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0699a-189">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="0699a-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0699a-190">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="0699a-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0699a-191">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="0699a-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0699a-192">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0699a-193">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="0699a-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-194">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-195">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0699a-196">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0699a-197">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0699a-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0699a-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0699a-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="0699a-199">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-200">Az.EventHub</span></span>
* <span data-ttu-id="0699a-201">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0699a-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0699a-202">Az.HDInsight</span></span>
* <span data-ttu-id="0699a-203">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0699a-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0699a-204">Az.MachineLearning</span></span>
* <span data-ttu-id="0699a-205">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0699a-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0699a-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0699a-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0699a-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0699a-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0699a-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0699a-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0699a-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0699a-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0699a-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0699a-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0699a-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0699a-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0699a-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0699a-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-213">Az.Network</span></span>
* <span data-ttu-id="0699a-214">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="0699a-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-216">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="0699a-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0699a-217">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="0699a-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0699a-218">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="0699a-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0699a-219">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="0699a-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-220">Az.Resources</span></span>
* <span data-ttu-id="0699a-221">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-222">Az.Sql</span></span>
* <span data-ttu-id="0699a-223">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="0699a-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0699a-224">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0699a-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0699a-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0699a-226">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-227">Az.Storage</span></span>
* <span data-ttu-id="0699a-228">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="0699a-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0699a-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0699a-230">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="0699a-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="0699a-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0699a-232">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0699a-233">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-233">General</span></span>
* <span data-ttu-id="0699a-234">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-235">Az.Accounts</span></span>
* <span data-ttu-id="0699a-236">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="0699a-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0699a-237">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="0699a-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0699a-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0699a-238">Az.Batch</span></span>
* <span data-ttu-id="0699a-239">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="0699a-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-240">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-241">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0699a-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0699a-242">Az.FrontDoor</span></span>
* <span data-ttu-id="0699a-243">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0699a-244">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0699a-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0699a-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="0699a-246">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="0699a-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-247">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-248">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0699a-249">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="0699a-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0699a-250">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-251">Az.Monitor</span></span>
* <span data-ttu-id="0699a-252">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0699a-253">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="0699a-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0699a-254">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="0699a-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-255">Az.Network</span></span>
* <span data-ttu-id="0699a-256">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="0699a-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-257">Az.Resources</span></span>
* <span data-ttu-id="0699a-258">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="0699a-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0699a-259">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="0699a-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-260">Az.Sql</span></span>
* <span data-ttu-id="0699a-261">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-262">Az.Storage</span></span>
* <span data-ttu-id="0699a-263">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0699a-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0699a-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0699a-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0699a-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0699a-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0699a-266">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="0699a-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0699a-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0699a-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0699a-268">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0699a-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0699a-269">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="0699a-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0699a-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0699a-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0699a-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0699a-272">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0699a-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0699a-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0699a-274">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="0699a-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0699a-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0699a-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0699a-276">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0699a-277">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0699a-277">Highlights since the last major release</span></span>
* <span data-ttu-id="0699a-278">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="0699a-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0699a-279">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="0699a-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-280">Az.Compute</span></span>
* <span data-ttu-id="0699a-281">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="0699a-281">VM Reapply feature</span></span>
    - <span data-ttu-id="0699a-282">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0699a-283">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="0699a-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0699a-284">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0699a-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0699a-285">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="0699a-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0699a-286">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0699a-287">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0699a-288">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0699a-289">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0699a-290">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0699a-291">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0699a-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0699a-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0699a-293">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0699a-294">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="0699a-294">Get the Order</span></span>
* <span data-ttu-id="0699a-295">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0699a-296">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="0699a-296">Create new Order</span></span>
* <span data-ttu-id="0699a-297">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0699a-298">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="0699a-298">Remove the Order</span></span>
* <span data-ttu-id="0699a-299">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="0699a-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0699a-300">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="0699a-300">Now creates Local Share</span></span>
* <span data-ttu-id="0699a-301">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0699a-302">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0699a-303">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0699a-304">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="0699a-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0699a-305">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0699a-306">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="0699a-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="0699a-307">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0699a-308">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="0699a-308">Create new Triggers</span></span>
* <span data-ttu-id="0699a-309">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0699a-310">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="0699a-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-311">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-312">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0699a-313">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0699a-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-315">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-316">Az.EventHub</span></span>
* <span data-ttu-id="0699a-317">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0699a-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0699a-318">Az.FrontDoor</span></span>
* <span data-ttu-id="0699a-319">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0699a-320">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0699a-321">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0699a-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0699a-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-323">Az.Network</span></span>
* <span data-ttu-id="0699a-324">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0699a-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0699a-325">Az.PrivateDns</span></span>
* <span data-ttu-id="0699a-326">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-328">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="0699a-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0699a-329">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="0699a-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0699a-330">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="0699a-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0699a-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0699a-331">Az.RedisCache</span></span>
* <span data-ttu-id="0699a-332">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0699a-333">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0699a-334">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-335">Az.Resources</span></span>
- <span data-ttu-id="0699a-336">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0699a-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0699a-337">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="0699a-338">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0699a-339">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="0699a-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0699a-340">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0699a-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-341">Az.Sql</span></span>
* <span data-ttu-id="0699a-342">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0699a-343">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="0699a-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0699a-344">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0699a-345">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-345">General</span></span>
* <span data-ttu-id="0699a-346">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="0699a-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-347">Az.Accounts</span></span>
* <span data-ttu-id="0699a-348">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0699a-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0699a-349">Az.Advisor</span></span>
* <span data-ttu-id="0699a-350">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0699a-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0699a-351">Az.Batch</span></span>
* <span data-ttu-id="0699a-352">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0699a-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0699a-353">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0699a-354">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="0699a-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0699a-355">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0699a-356">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0699a-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0699a-357">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0699a-358">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0699a-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0699a-359">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0699a-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0699a-360">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0699a-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0699a-361">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0699a-362">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0699a-363">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0699a-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0699a-364">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0699a-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0699a-365">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="0699a-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0699a-366">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0699a-367">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0699a-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0699a-368">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0699a-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0699a-369">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0699a-370">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0699a-371">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0699a-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="0699a-372">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0699a-373">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0699a-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0699a-374">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0699a-375">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0699a-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="0699a-376">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="0699a-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0699a-377">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0699a-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="0699a-378">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0699a-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0699a-379">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0699a-380">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="0699a-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0699a-381">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="0699a-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0699a-382">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="0699a-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0699a-383">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0699a-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0699a-384">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0699a-385">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="0699a-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0699a-386">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="0699a-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0699a-387">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="0699a-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0699a-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-388">Az.Cdn</span></span>
* <span data-ttu-id="0699a-389">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0699a-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0699a-390">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="0699a-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-391">Az.Compute</span></span>
* <span data-ttu-id="0699a-392">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="0699a-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0699a-393">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0699a-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0699a-394">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="0699a-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="0699a-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0699a-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0699a-396">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0699a-397">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0699a-398">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="0699a-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0699a-399">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0699a-400">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="0699a-400">Breaking changes</span></span>
    - <span data-ttu-id="0699a-401">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0699a-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0699a-402">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0699a-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-403">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-404">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-406">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="0699a-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0699a-407">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="0699a-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0699a-408">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="0699a-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0699a-409">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="0699a-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0699a-410">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="0699a-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0699a-411">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="0699a-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0699a-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0699a-412">Az.FrontDoor</span></span>
* <span data-ttu-id="0699a-413">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0699a-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0699a-414">Az.HDInsight</span></span>
* <span data-ttu-id="0699a-415">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="0699a-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0699a-416">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0699a-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0699a-417">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0699a-418">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="0699a-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0699a-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0699a-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0699a-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0699a-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0699a-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0699a-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0699a-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0699a-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0699a-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0699a-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0699a-424">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="0699a-425">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="0699a-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0699a-426">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="0699a-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0699a-427">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="0699a-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0699a-428">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0699a-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0699a-429">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0699a-430">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0699a-431">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="0699a-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0699a-432">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0699a-433">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0699a-434">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0699a-435">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="0699a-436">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="0699a-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-437">Az.IotHub</span></span>
* <span data-ttu-id="0699a-438">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="0699a-438">Breaking changes:</span></span>
    - <span data-ttu-id="0699a-439">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0699a-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0699a-440">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0699a-441">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0699a-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0699a-442">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0699a-443">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0699a-444">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0699a-445">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="0699a-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0699a-446">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="0699a-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0699a-447">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0699a-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0699a-448">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0699a-449">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0699a-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0699a-450">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-452">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-453">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0699a-454">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0699a-455">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-456">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-457">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-458">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-459">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-460">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-461">Az.Resources</span></span>
* <span data-ttu-id="0699a-462">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-463">Az.Network</span></span>
* <span data-ttu-id="0699a-464">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0699a-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0699a-465">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0699a-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="0699a-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0699a-471">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="0699a-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0699a-472">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0699a-472">New cmdlet:</span></span>
        - <span data-ttu-id="0699a-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0699a-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0699a-474">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0699a-475">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0699a-476">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0699a-477">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0699a-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0699a-478">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0699a-479">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0699a-480">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0699a-481">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-481">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0699a-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0699a-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0699a-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0699a-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0699a-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0699a-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0699a-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0699a-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0699a-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0699a-487">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0699a-488">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0699a-489">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0699a-490">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0699a-491">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0699a-492">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0699a-493">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0699a-494">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-494">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0699a-496">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0699a-497">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0699a-498">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0699a-499">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0699a-500">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0699a-501">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0699a-502">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0699a-503">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-503">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0699a-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0699a-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0699a-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0699a-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0699a-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0699a-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0699a-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0699a-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0699a-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0699a-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0699a-510">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0699a-511">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0699a-512">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0699a-513">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0699a-514">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0699a-515">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0699a-516">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0699a-517">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0699a-518">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="0699a-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0699a-519">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0699a-520">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0699a-521">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-521">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0699a-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="0699a-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0699a-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0699a-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0699a-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0699a-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0699a-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-527">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="0699a-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-528">Az.Sql</span></span>
* <span data-ttu-id="0699a-529">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0699a-530">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="0699a-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0699a-531">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="0699a-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0699a-532">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="0699a-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0699a-533">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="0699a-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0699a-534">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0699a-535">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0699a-536">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="0699a-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="0699a-537">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-538">Az.Storage</span></span>
* <span data-ttu-id="0699a-539">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0699a-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0699a-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0699a-542">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0699a-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0699a-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0699a-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0699a-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0699a-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="0699a-545">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0699a-546">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-546">General</span></span>
* <span data-ttu-id="0699a-547">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0699a-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-548">Az.Accounts</span></span>
* <span data-ttu-id="0699a-549">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0699a-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-550">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-551">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0699a-552">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="0699a-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-553">Az.Automation</span></span>
* <span data-ttu-id="0699a-554">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="0699a-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0699a-555">Az.Batch</span></span>
* <span data-ttu-id="0699a-556">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0699a-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-557">Az.Compute</span></span>
* <span data-ttu-id="0699a-558">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0699a-559">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0699a-560">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="0699a-561">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="0699a-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-562">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-563">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="0699a-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0699a-564">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0699a-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0699a-565">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-567">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="0699a-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0699a-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0699a-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="0699a-569">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0699a-570">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0699a-571">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="0699a-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0699a-572">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-573">Az.IotHub</span></span>
* <span data-ttu-id="0699a-574">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0699a-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0699a-575">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="0699a-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="0699a-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-576">Az.Monitor</span></span>
* <span data-ttu-id="0699a-577">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0699a-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0699a-578">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0699a-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0699a-579">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="0699a-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0699a-580">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0699a-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-581">Az.Network</span></span>
* <span data-ttu-id="0699a-582">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="0699a-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0699a-583">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0699a-584">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-584">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0699a-586">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0699a-587">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0699a-588">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="0699a-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0699a-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0699a-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0699a-592">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0699a-593">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0699a-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0699a-594">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0699a-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0699a-595">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0699a-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0699a-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0699a-596">Az.RedisCache</span></span>
* <span data-ttu-id="0699a-597">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="0699a-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-598">Az.Sql</span></span>
* <span data-ttu-id="0699a-599">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-600">Az.Storage</span></span>
* <span data-ttu-id="0699a-601">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0699a-602">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="0699a-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0699a-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0699a-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0699a-604">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="0699a-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0699a-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0699a-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0699a-606">Az.StorageSync</span></span>
* <span data-ttu-id="0699a-607">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-608">Az.Websites</span></span>
* <span data-ttu-id="0699a-609">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="0699a-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0699a-610">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0699a-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-611">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-612">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0699a-613">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0699a-614">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="0699a-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-615">Az.Automation</span></span>
* <span data-ttu-id="0699a-616">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0699a-617">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0699a-618">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-619">Az.Compute</span></span>
* <span data-ttu-id="0699a-620">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0699a-621">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0699a-622">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0699a-623">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0699a-624">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0699a-625">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="0699a-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0699a-626">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0699a-627">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0699a-628">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-629">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-630">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0699a-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0699a-631">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0699a-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0699a-632">Az.HDInsight</span></span>
* <span data-ttu-id="0699a-633">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-634">Az.IotHub</span></span>
* <span data-ttu-id="0699a-635">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0699a-636">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0699a-637">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="0699a-637">New cmdlets are:</span></span>
    - <span data-ttu-id="0699a-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0699a-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0699a-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0699a-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0699a-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0699a-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0699a-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0699a-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-642">Az.Monitor</span></span>
* <span data-ttu-id="0699a-643">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="0699a-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0699a-644">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="0699a-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0699a-645">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0699a-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0699a-646">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="0699a-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0699a-647">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="0699a-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0699a-648">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="0699a-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0699a-649">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="0699a-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0699a-650">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0699a-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0699a-651">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0699a-652">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0699a-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0699a-653">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0699a-654">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0699a-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0699a-655">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="0699a-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0699a-656">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="0699a-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0699a-657">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="0699a-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0699a-658">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="0699a-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0699a-659">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="0699a-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0699a-660">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="0699a-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0699a-661">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0699a-662">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="0699a-662">Overall improved help files</span></span>
* <span data-ttu-id="0699a-663">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-664">Az.Network</span></span>
* <span data-ttu-id="0699a-665">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="0699a-666">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0699a-667">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="0699a-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0699a-668">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="0699a-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0699a-669">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="0699a-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0699a-670">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0699a-671">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0699a-672">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0699a-673">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0699a-674">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0699a-675">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0699a-676">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="0699a-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0699a-677">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-677">New cmdlets</span></span>
        - <span data-ttu-id="0699a-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0699a-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0699a-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0699a-680">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0699a-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="0699a-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0699a-681">New-VpnSite</span></span>
        - <span data-ttu-id="0699a-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0699a-682">Update-VpnSite</span></span>
        - <span data-ttu-id="0699a-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-683">New-VpnConnection</span></span>
        - <span data-ttu-id="0699a-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-684">Update-VpnConnection</span></span>
* <span data-ttu-id="0699a-685">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0699a-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-687">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0699a-688">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-689">Az.Resources</span></span>
* <span data-ttu-id="0699a-690">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="0699a-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-692">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0699a-693">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0699a-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0699a-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0699a-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0699a-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0699a-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0699a-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0699a-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0699a-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0699a-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0699a-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0699a-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0699a-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0699a-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0699a-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0699a-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0699a-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0699a-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0699a-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0699a-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0699a-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0699a-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0699a-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0699a-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0699a-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0699a-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0699a-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0699a-707">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="0699a-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0699a-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0699a-708">Az.SignalR</span></span>
* <span data-ttu-id="0699a-709">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-710">Az.Sql</span></span>
* <span data-ttu-id="0699a-711">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0699a-712">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="0699a-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0699a-713">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="0699a-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0699a-714">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="0699a-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0699a-715">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="0699a-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-716">Az.Storage</span></span>
* <span data-ttu-id="0699a-717">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0699a-718">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0699a-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0699a-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0699a-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0699a-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0699a-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0699a-721">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0699a-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0699a-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0699a-723">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="0699a-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0699a-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0699a-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0699a-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0699a-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0699a-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0699a-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0699a-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0699a-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-728">Az.Websites</span></span>
* <span data-ttu-id="0699a-729">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="0699a-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0699a-730">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0699a-731">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0699a-732">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0699a-733">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-733">General</span></span>
* <span data-ttu-id="0699a-734">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-735">Az.Accounts</span></span>
* <span data-ttu-id="0699a-736">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="0699a-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0699a-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0699a-737">Az.Aks</span></span>
* <span data-ttu-id="0699a-738">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0699a-739">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0699a-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0699a-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-740">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-741">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="0699a-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0699a-742">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="0699a-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0699a-743">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0699a-744">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0699a-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0699a-745">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0699a-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0699a-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0699a-746">Az.Batch</span></span>
* <span data-ttu-id="0699a-747">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="0699a-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0699a-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-748">Az.Cdn</span></span>
* <span data-ttu-id="0699a-749">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-750">Az.Compute</span></span>
* <span data-ttu-id="0699a-751">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0699a-752">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0699a-753">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0699a-754">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0699a-755">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0699a-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0699a-756">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0699a-757">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0699a-758">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-759">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-760">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="0699a-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0699a-761">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0699a-762">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="0699a-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0699a-763">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-765">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-766">Az.EventHub</span></span>
* <span data-ttu-id="0699a-767">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="0699a-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0699a-768">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="0699a-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0699a-769">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0699a-770">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="0699a-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0699a-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0699a-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0699a-772">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-773">Az.Monitor</span></span>
* <span data-ttu-id="0699a-774">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-775">Az.Network</span></span>
* <span data-ttu-id="0699a-776">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0699a-777">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="0699a-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0699a-778">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="0699a-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0699a-779">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0699a-780">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="0699a-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="0699a-781">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0699a-782">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="0699a-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="0699a-784">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="0699a-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0699a-785">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-785">Added example</span></span>
    - <span data-ttu-id="0699a-786">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0699a-787">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0699a-788">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-790">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-791">Az.Resources</span></span>
* <span data-ttu-id="0699a-792">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0699a-793">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0699a-794">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0699a-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0699a-795">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0699a-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0699a-796">Az.ServiceBus</span></span>
* <span data-ttu-id="0699a-797">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="0699a-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0699a-798">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="0699a-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0699a-799">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-801">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="0699a-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0699a-802">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="0699a-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0699a-803">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0699a-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0699a-804">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="0699a-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0699a-805">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0699a-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0699a-806">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="0699a-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-807">Az.Sql</span></span>
* <span data-ttu-id="0699a-808">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-809">Az.Storage</span></span>
* <span data-ttu-id="0699a-810">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="0699a-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0699a-811">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="0699a-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0699a-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0699a-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0699a-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0699a-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0699a-814">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="0699a-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0699a-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0699a-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-816">Az.Websites</span></span>
* <span data-ttu-id="0699a-817">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="0699a-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0699a-818">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-819">Az.Accounts</span></span>
* <span data-ttu-id="0699a-820">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0699a-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0699a-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0699a-822">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="0699a-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-823">Az.Automation</span></span>
* <span data-ttu-id="0699a-824">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="0699a-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0699a-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="0699a-826">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-827">Az.Compute</span></span>
* <span data-ttu-id="0699a-828">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0699a-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0699a-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0699a-830">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0699a-831">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="0699a-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-832">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-833">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0699a-834">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-835">Az.EventHub</span></span>
* <span data-ttu-id="0699a-836">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0699a-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0699a-837">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="0699a-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-838">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-839">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0699a-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0699a-840">Az.LogicApp</span></span>
* <span data-ttu-id="0699a-841">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="0699a-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0699a-842">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0699a-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0699a-843">Az.ManagedServices</span></span>
* <span data-ttu-id="0699a-844">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-845">Az.Network</span></span>
* <span data-ttu-id="0699a-846">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0699a-847">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-847">New cmdlets</span></span>
        - <span data-ttu-id="0699a-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0699a-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0699a-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0699a-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0699a-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0699a-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0699a-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0699a-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0699a-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0699a-856">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0699a-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0699a-857">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0699a-858">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="0699a-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0699a-859">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="0699a-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0699a-860">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0699a-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0699a-861">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="0699a-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0699a-862">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-862">Updated cmdlets</span></span>
        - <span data-ttu-id="0699a-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0699a-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0699a-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0699a-866">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0699a-867">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0699a-868">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0699a-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="0699a-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0699a-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0699a-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0699a-872">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0699a-873">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0699a-874">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="0699a-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="0699a-876">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="0699a-877">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-879">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0699a-880">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0699a-881">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0699a-882">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0699a-883">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0699a-884">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0699a-885">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0699a-886">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0699a-887">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0699a-888">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-889">Az.Resources</span></span>
- <span data-ttu-id="0699a-890">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="0699a-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0699a-891">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0699a-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0699a-892">Az.ServiceBus</span></span>
* <span data-ttu-id="0699a-893">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0699a-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0699a-894">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="0699a-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-895">Az.Sql</span></span>
* <span data-ttu-id="0699a-896">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0699a-897">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0699a-898">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-899">Az.Storage</span></span>
* <span data-ttu-id="0699a-900">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0699a-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0699a-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0699a-901">Az.StorageSync</span></span>
* <span data-ttu-id="0699a-902">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0699a-903">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-904">Az.Websites</span></span>
* <span data-ttu-id="0699a-905">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="0699a-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0699a-906">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0699a-907">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0699a-908">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-909">Az.Accounts</span></span>
* <span data-ttu-id="0699a-910">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0699a-911">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0699a-912">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="0699a-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0699a-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0699a-913">Az.Advisor</span></span>
* <span data-ttu-id="0699a-914">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0699a-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0699a-915">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="0699a-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0699a-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-916">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-917">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="0699a-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0699a-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0699a-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0699a-919">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0699a-920">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="0699a-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0699a-921">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="0699a-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0699a-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0699a-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0699a-923">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-924">Az.Automation</span></span>
* <span data-ttu-id="0699a-925">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-926">Az.Compute</span></span>
* <span data-ttu-id="0699a-927">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-928">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-929">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0699a-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0699a-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0699a-930">Az.EventGrid</span></span>
* <span data-ttu-id="0699a-931">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-932">Az.IotHub</span></span>
* <span data-ttu-id="0699a-933">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-934">Az.Network</span></span>
* <span data-ttu-id="0699a-935">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0699a-936">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0699a-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0699a-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="0699a-938">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="0699a-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0699a-939">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0699a-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="0699a-941">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-943">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="0699a-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-944">Az.Resources</span></span>
    - <span data-ttu-id="0699a-945">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0699a-946">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0699a-947">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0699a-948">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0699a-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0699a-949">Az.ServiceBus</span></span>
* <span data-ttu-id="0699a-950">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="0699a-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-951">Az.Sql</span></span>
* <span data-ttu-id="0699a-952">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0699a-953">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0699a-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0699a-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0699a-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0699a-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0699a-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0699a-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0699a-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0699a-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0699a-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0699a-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0699a-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0699a-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0699a-960">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-961">Az.Storage</span></span>
* <span data-ttu-id="0699a-962">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="0699a-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0699a-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0699a-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0699a-964">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="0699a-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0699a-965">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="0699a-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0699a-966">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0699a-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0699a-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0699a-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0699a-969">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="0699a-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0699a-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0699a-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0699a-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0699a-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0699a-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0699a-972">Az.StorageSync</span></span>
* <span data-ttu-id="0699a-973">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="0699a-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0699a-974">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-975">Az.Accounts</span></span>
* <span data-ttu-id="0699a-976">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="0699a-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0699a-977">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0699a-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0699a-978">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0699a-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0699a-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0699a-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0699a-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-981">Az.Compute</span></span>
* <span data-ttu-id="0699a-982">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="0699a-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0699a-983">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0699a-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0699a-984">Az.Dns</span></span>
* <span data-ttu-id="0699a-985">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0699a-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0699a-986">Az.EventGrid</span></span>
* <span data-ttu-id="0699a-987">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0699a-988">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-988">New cmdlets:</span></span>
    - <span data-ttu-id="0699a-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0699a-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0699a-990">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="0699a-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0699a-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0699a-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0699a-992">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0699a-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0699a-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0699a-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0699a-994">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="0699a-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0699a-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0699a-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0699a-996">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="0699a-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0699a-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0699a-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0699a-998">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0699a-999">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0699a-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0699a-1000">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="0699a-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0699a-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0699a-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0699a-1002">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0699a-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="0699a-1003">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0699a-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0699a-1004">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="0699a-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0699a-1005">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="0699a-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0699a-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0699a-1007">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="0699a-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0699a-1008">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="0699a-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0699a-1009">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="0699a-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0699a-1010">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0699a-1011">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="0699a-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0699a-1012">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="0699a-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0699a-1013">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0699a-1014">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="0699a-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="0699a-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0699a-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0699a-1016">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0699a-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0699a-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0699a-1018">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="0699a-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0699a-1019">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="0699a-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0699a-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0699a-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="0699a-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0699a-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0699a-1022">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0699a-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0699a-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0699a-1024">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1025">Az.Network</span></span>
* <span data-ttu-id="0699a-1026">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0699a-1027">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1027">New cmdlets</span></span>
        - <span data-ttu-id="0699a-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0699a-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0699a-1029">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0699a-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0699a-1030">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1030">New cmdlets</span></span> 
        - <span data-ttu-id="0699a-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0699a-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0699a-1032">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0699a-1033">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1033">New cmdlets</span></span> 
        - <span data-ttu-id="0699a-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0699a-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="0699a-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0699a-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0699a-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0699a-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0699a-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0699a-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0699a-1039">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0699a-1040">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1040">New cmdlets</span></span>
        - <span data-ttu-id="0699a-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0699a-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0699a-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0699a-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0699a-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0699a-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0699a-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0699a-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0699a-1045">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="0699a-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0699a-1046">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="0699a-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0699a-1047">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="0699a-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0699a-1048">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0699a-1049">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0699a-1050">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="0699a-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0699a-1051">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0699a-1052">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="0699a-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0699a-1053">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0699a-1054">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0699a-1055">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="0699a-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0699a-1056">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0699a-1057">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0699a-1058">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0699a-1059">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="0699a-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0699a-1060">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0699a-1061">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0699a-1062">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="0699a-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0699a-1063">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="0699a-1064">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="0699a-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="0699a-1065">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0699a-1066">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0699a-1067">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="0699a-1069">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="0699a-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1070">Az.Resources</span></span>
* <span data-ttu-id="0699a-1071">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0699a-1072">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0699a-1073">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0699a-1074">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="0699a-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-1076">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="0699a-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1077">Az.Sql</span></span>
* <span data-ttu-id="0699a-1078">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0699a-1079">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0699a-1080">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0699a-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0699a-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0699a-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0699a-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0699a-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0699a-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0699a-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0699a-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0699a-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0699a-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1086">Az.Storage</span></span>
* <span data-ttu-id="0699a-1087">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0699a-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0699a-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="0699a-1089">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="0699a-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0699a-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1091">Az.Websites</span></span>
* <span data-ttu-id="0699a-1092">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="0699a-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0699a-1093">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0699a-1094">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0699a-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-1095">Az.Cdn</span></span>
* <span data-ttu-id="0699a-1096">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1097">Az.Compute</span></span>
* <span data-ttu-id="0699a-1098">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0699a-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0699a-1099">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0699a-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-1100">Az.EventHub</span></span>
* <span data-ttu-id="0699a-1101">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="0699a-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0699a-1102">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="0699a-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1103">Az.Network</span></span>
* <span data-ttu-id="0699a-1104">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0699a-1105">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0699a-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="0699a-1107">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0699a-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-1109">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0699a-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0699a-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="0699a-1111">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="0699a-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-1113">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0699a-1114">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1115">Az.Sql</span></span>
* <span data-ttu-id="0699a-1116">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0699a-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0699a-1117">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0699a-1118">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="0699a-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0699a-1119">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="0699a-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1120">Az.Websites</span></span>
* <span data-ttu-id="0699a-1121">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0699a-1122">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0699a-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-1124">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0699a-1125">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="0699a-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0699a-1126">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="0699a-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0699a-1127">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="0699a-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0699a-1128">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="0699a-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0699a-1129">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="0699a-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0699a-1130">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="0699a-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0699a-1131">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="0699a-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0699a-1132">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0699a-1133">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="0699a-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0699a-1134">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="0699a-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0699a-1135">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="0699a-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0699a-1136">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="0699a-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0699a-1137">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0699a-1138">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="0699a-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0699a-1139">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="0699a-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0699a-1140">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="0699a-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0699a-1141">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="0699a-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0699a-1142">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="0699a-1143">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="0699a-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0699a-1144">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0699a-1145">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="0699a-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0699a-1146">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="0699a-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0699a-1147">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="0699a-1148">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0699a-1149">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0699a-1150">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="0699a-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0699a-1151">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0699a-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0699a-1152">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0699a-1153">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="0699a-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0699a-1154">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="0699a-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="0699a-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0699a-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0699a-1156">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0699a-1157">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0699a-1158">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="0699a-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0699a-1159">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="0699a-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0699a-1160">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="0699a-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0699a-1161">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="0699a-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0699a-1162">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="0699a-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0699a-1163">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="0699a-1164">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="0699a-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0699a-1165">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="0699a-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0699a-1166">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="0699a-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0699a-1167">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="0699a-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0699a-1168">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0699a-1169">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="0699a-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0699a-1170">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="0699a-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="0699a-1171">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="0699a-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0699a-1172">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0699a-1173">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="0699a-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0699a-1174">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="0699a-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0699a-1175">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="0699a-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0699a-1176">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="0699a-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0699a-1177">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0699a-1178">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="0699a-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0699a-1179">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="0699a-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0699a-1180">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0699a-1181">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="0699a-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0699a-1182">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="0699a-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0699a-1183">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0699a-1184">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0699a-1185">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="0699a-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0699a-1186">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="0699a-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0699a-1187">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0699a-1188">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="0699a-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0699a-1189">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="0699a-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0699a-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0699a-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0699a-1191">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="0699a-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0699a-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0699a-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0699a-1193">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0699a-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0699a-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0699a-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0699a-1195">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0699a-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0699a-1196">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="0699a-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0699a-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0699a-1198">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="0699a-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="0699a-1199">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0699a-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0699a-1200">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="0699a-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1201">Az.Automation</span></span>
* <span data-ttu-id="0699a-1202">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0699a-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0699a-1203">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="0699a-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0699a-1204">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="0699a-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0699a-1205">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="0699a-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0699a-1206">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="0699a-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0699a-1207">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="0699a-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0699a-1208">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="0699a-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1209">Az.Compute</span></span>
* <span data-ttu-id="0699a-1210">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0699a-1211">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1213">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="0699a-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-1214">Az.Monitor</span></span>
* <span data-ttu-id="0699a-1215">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="0699a-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1216">Az.Network</span></span>
* <span data-ttu-id="0699a-1217">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0699a-1218">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0699a-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="0699a-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0699a-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0699a-1220">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0699a-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1221">Az.Resources</span></span>
* <span data-ttu-id="0699a-1222">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1223">Az.Sql</span></span>
* <span data-ttu-id="0699a-1224">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="0699a-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0699a-1225">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1226">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1227">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="0699a-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0699a-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="0699a-1229">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="0699a-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0699a-1230">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="0699a-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1231">Az.Compute</span></span>
* <span data-ttu-id="0699a-1232">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0699a-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0699a-1233">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0699a-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0699a-1234">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0699a-1235">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0699a-1236">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="0699a-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0699a-1237">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="0699a-1238">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="0699a-1238">Breaking changes</span></span>
    - <span data-ttu-id="0699a-1239">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0699a-1240">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0699a-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0699a-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="0699a-1242">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0699a-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0699a-1243">Az.Dns</span></span>
* <span data-ttu-id="0699a-1244">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="0699a-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0699a-1245">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="0699a-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0699a-1246">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0699a-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0699a-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="0699a-1248">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0699a-1249">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="0699a-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0699a-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0699a-1250">Az.HDInsight</span></span>
* <span data-ttu-id="0699a-1251">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="0699a-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0699a-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0699a-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0699a-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0699a-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0699a-1254">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="0699a-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0699a-1255">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="0699a-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0699a-1256">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0699a-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0699a-1257">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-1258">Az.Monitor</span></span>
* <span data-ttu-id="0699a-1259">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="0699a-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="0699a-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0699a-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0699a-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0699a-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0699a-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0699a-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0699a-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0699a-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0699a-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0699a-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0699a-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0699a-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0699a-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0699a-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0699a-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0699a-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0699a-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0699a-1271">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="0699a-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0699a-1272">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="0699a-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1273">Az.Network</span></span>
* <span data-ttu-id="0699a-1274">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0699a-1275">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1275">New cmdlets</span></span>
        - <span data-ttu-id="0699a-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0699a-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="0699a-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0699a-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0699a-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0699a-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0699a-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0699a-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0699a-1280">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="0699a-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0699a-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0699a-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0699a-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0699a-1283">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0699a-1284">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="0699a-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0699a-1285">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="0699a-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0699a-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="0699a-1287">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="0699a-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0699a-1288">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0699a-1289">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="0699a-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-1291">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="0699a-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0699a-1292">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="0699a-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0699a-1293">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="0699a-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0699a-1294">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="0699a-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0699a-1295">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="0699a-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0699a-1296">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="0699a-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0699a-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0699a-1297">Az.Relay</span></span>
* <span data-ttu-id="0699a-1298">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="0699a-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0699a-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0699a-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="0699a-1300">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1301">Az.Storage</span></span>
* <span data-ttu-id="0699a-1302">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="0699a-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0699a-1303">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0699a-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0699a-1304">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0699a-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="0699a-1306">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="0699a-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0699a-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0699a-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0699a-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1310">Az.Websites</span></span>
* <span data-ttu-id="0699a-1311">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0699a-1312">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0699a-1313">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0699a-1314">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0699a-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="0699a-1315">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="0699a-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="0699a-1316">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="0699a-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0699a-1317">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="0699a-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0699a-1318">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0699a-1319">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0699a-1320">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0699a-1321">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1322">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1323">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="0699a-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0699a-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0699a-1324">Az.Batch</span></span>
* <span data-ttu-id="0699a-1325">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0699a-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-1326">Az.Cdn</span></span>
* <span data-ttu-id="0699a-1327">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0699a-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="0699a-1329">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1330">Az.Compute</span></span>
* <span data-ttu-id="0699a-1331">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="0699a-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0699a-1332">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0699a-1333">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-1334">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-1335">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="0699a-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1337">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0699a-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0699a-1338">Az.EventGrid</span></span>
* <span data-ttu-id="0699a-1339">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0699a-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-1340">Az.EventHub</span></span>
* <span data-ttu-id="0699a-1341">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0699a-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0699a-1342">Az.HDInsight</span></span>
* <span data-ttu-id="0699a-1343">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-1344">Az.IotHub</span></span>
* <span data-ttu-id="0699a-1345">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-1346">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-1347">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0699a-1348">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0699a-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0699a-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="0699a-1350">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0699a-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0699a-1351">Az.Media</span></span>
* <span data-ttu-id="0699a-1352">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-1353">Az.Monitor</span></span>
  * <span data-ttu-id="0699a-1354">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="0699a-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0699a-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0699a-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0699a-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0699a-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0699a-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0699a-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0699a-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0699a-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0699a-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0699a-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0699a-1360">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1361">Az.Network</span></span>
* <span data-ttu-id="0699a-1362">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0699a-1363">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0699a-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0699a-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="0699a-1365">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="0699a-1367">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0699a-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0699a-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0699a-1369">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-1371">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0699a-1372">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0699a-1373">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0699a-1374">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0699a-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0699a-1375">Az.RedisCache</span></span>
* <span data-ttu-id="0699a-1376">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1377">Az.Resources</span></span>
* <span data-ttu-id="0699a-1378">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1379">Az.Sql</span></span>
* <span data-ttu-id="0699a-1380">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="0699a-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0699a-1381">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0699a-1382">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="0699a-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0699a-1383">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0699a-1384">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="0699a-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0699a-1385">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="0699a-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0699a-1386">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1387">Az.Websites</span></span>
* <span data-ttu-id="0699a-1388">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="0699a-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0699a-1389">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0699a-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0699a-1390">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0699a-1391">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0699a-1392">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0699a-1393">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0699a-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="0699a-1394">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="0699a-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="0699a-1395">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="0699a-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0699a-1396">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="0699a-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0699a-1397">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0699a-1398">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0699a-1399">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0699a-1400">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0699a-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1401">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1402">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="0699a-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0699a-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="0699a-1404">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0699a-1405">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0699a-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1406">Az.Automation</span></span>
* <span data-ttu-id="0699a-1407">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="0699a-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0699a-1408">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0699a-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0699a-1409">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="0699a-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1410">Az.Compute</span></span>
* <span data-ttu-id="0699a-1411">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0699a-1412">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="0699a-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0699a-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="0699a-1414">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="0699a-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-1415">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-1416">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0699a-1417">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1418">Az.Resources</span></span>
* <span data-ttu-id="0699a-1419">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0699a-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0699a-1420">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0699a-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0699a-1421">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="0699a-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0699a-1422">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0699a-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0699a-1423">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="0699a-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0699a-1424">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0699a-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1425">Az.Sql</span></span>
* <span data-ttu-id="0699a-1426">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="0699a-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1427">Az.Storage</span></span>
* <span data-ttu-id="0699a-1428">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="0699a-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0699a-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0699a-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="0699a-1430">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="0699a-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0699a-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0699a-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0699a-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0699a-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0699a-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0699a-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0699a-1435">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="0699a-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0699a-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0699a-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0699a-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0699a-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0699a-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0699a-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0699a-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0699a-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0699a-1440">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0699a-1441">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0699a-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="0699a-1442">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="0699a-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="0699a-1443">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="0699a-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0699a-1444">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="0699a-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0699a-1445">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0699a-1446">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0699a-1447">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0699a-1448">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1449">Az.Automation</span></span>
* <span data-ttu-id="0699a-1450">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="0699a-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0699a-1451">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="0699a-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="0699a-1452">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="0699a-1452">Pre-Post script</span></span>
    * <span data-ttu-id="0699a-1453">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="0699a-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1454">Az.Compute</span></span>
* <span data-ttu-id="0699a-1455">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0699a-1456">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-1457">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-1458">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1459">Az.Network</span></span>
* <span data-ttu-id="0699a-1460">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0699a-1461">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-1463">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0699a-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0699a-1464">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1465">Az.Resources</span></span>
* <span data-ttu-id="0699a-1466">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0699a-1467">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0699a-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1468">Az.Sql</span></span>
* <span data-ttu-id="0699a-1469">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1470">Az.Storage</span></span>
* <span data-ttu-id="0699a-1471">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0699a-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0699a-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0699a-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0699a-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0699a-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0699a-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0699a-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0699a-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0699a-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1478">Az.Websites</span></span>
* <span data-ttu-id="0699a-1479">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="0699a-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0699a-1480">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1481">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1482">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0699a-1483">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1484">Az.Automation</span></span>
* <span data-ttu-id="0699a-1485">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="0699a-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0699a-1486">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="0699a-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0699a-1487">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0699a-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0699a-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-1488">Az.Cdn</span></span>
* <span data-ttu-id="0699a-1489">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="0699a-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1490">Az.Compute</span></span>
* <span data-ttu-id="0699a-1491">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-1492">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-1493">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0699a-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0699a-1494">Az.LogicApp</span></span>
* <span data-ttu-id="0699a-1495">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0699a-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1496">Az.Network</span></span>
* <span data-ttu-id="0699a-1497">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-1499">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="0699a-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0699a-1500">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="0699a-1500">SDK Update</span></span>
* <span data-ttu-id="0699a-1501">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0699a-1502">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1503">Az.Resources</span></span>
* <span data-ttu-id="0699a-1504">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0699a-1505">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0699a-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0699a-1506">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0699a-1507">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0699a-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0699a-1508">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0699a-1509">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0699a-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1510">Az.Sql</span></span>
* <span data-ttu-id="0699a-1511">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0699a-1512">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1513">Az.Storage</span></span>
* <span data-ttu-id="0699a-1514">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0699a-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0699a-1515">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0699a-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="0699a-1517">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1518">Az.Automation</span></span>
* <span data-ttu-id="0699a-1519">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0699a-1520">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0699a-1521">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0699a-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0699a-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="0699a-1523">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1524">Az.Compute</span></span>
* <span data-ttu-id="0699a-1525">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0699a-1526">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="0699a-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0699a-1527">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0699a-1528">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="0699a-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1530">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0699a-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0699a-1531">Az.EventHub</span></span>
* <span data-ttu-id="0699a-1532">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-1533">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-1534">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0699a-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0699a-1535">Az.LogicApp</span></span>
* <span data-ttu-id="0699a-1536">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0699a-1537">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0699a-1538">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="0699a-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0699a-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0699a-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0699a-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0699a-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0699a-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0699a-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0699a-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0699a-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0699a-1543">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0699a-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0699a-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0699a-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0699a-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0699a-1548">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0699a-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-1549">Az.Monitor</span></span>
* <span data-ttu-id="0699a-1550">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1551">Az.Network</span></span>
* <span data-ttu-id="0699a-1552">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="0699a-1554">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0699a-1555">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0699a-1556">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="0699a-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0699a-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1557">Az.Resources</span></span>
* <span data-ttu-id="0699a-1558">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0699a-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0699a-1559">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0699a-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0699a-1560">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0699a-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0699a-1561">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="0699a-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1562">Az.Sql</span></span>
* <span data-ttu-id="0699a-1563">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0699a-1564">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="0699a-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1565">Az.Websites</span></span>
* <span data-ttu-id="0699a-1566">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0699a-1567">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1568">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1569">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="0699a-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0699a-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="0699a-1571">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="0699a-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1572">Az.Compute</span></span>
* <span data-ttu-id="0699a-1573">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0699a-1574">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0699a-1575">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="0699a-1577">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="0699a-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1578">Az.Resources</span></span>
* <span data-ttu-id="0699a-1579">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0699a-1580">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0699a-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0699a-1581">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0699a-1582">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0699a-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1583">Az.Sql</span></span>
* <span data-ttu-id="0699a-1584">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0699a-1585">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="0699a-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0699a-1586">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0699a-1587">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1588">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1589">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0699a-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0699a-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="0699a-1591">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="0699a-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="0699a-1593">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="0699a-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0699a-1594">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1595">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1596">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0699a-1597">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0699a-1598">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0699a-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0699a-1599">Az.Aks</span></span>
* <span data-ttu-id="0699a-1600">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0699a-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1601">Az.Automation</span></span>
* <span data-ttu-id="0699a-1602">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0699a-1603">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0699a-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0699a-1604">Az.Cdn</span></span>
* <span data-ttu-id="0699a-1605">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1606">Az.Compute</span></span>
* <span data-ttu-id="0699a-1607">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0699a-1608">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0699a-1609">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0699a-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0699a-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0699a-1611">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0699a-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0699a-1612">Az.DataFactory</span></span>
* <span data-ttu-id="0699a-1613">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1615">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0699a-1616">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0699a-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0699a-1617">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-1618">Az.IotHub</span></span>
* <span data-ttu-id="0699a-1619">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0699a-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-1620">Az.KeyVault</span></span>
* <span data-ttu-id="0699a-1621">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1622">Az.Network</span></span>
* <span data-ttu-id="0699a-1623">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1624">Az.Resources</span></span>
* <span data-ttu-id="0699a-1625">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0699a-1626">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="0699a-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0699a-1627">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="0699a-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0699a-1628">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0699a-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0699a-1629">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0699a-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0699a-1630">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0699a-1631">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0699a-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-1633">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0699a-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0699a-1634">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1634">Fix some error messages.</span></span>
* <span data-ttu-id="0699a-1635">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="0699a-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0699a-1636">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0699a-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0699a-1637">Az.SignalR</span></span>
* <span data-ttu-id="0699a-1638">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1639">Az.Sql</span></span>
* <span data-ttu-id="0699a-1640">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0699a-1641">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0699a-1642">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="0699a-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0699a-1643">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="0699a-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1644">Az.Storage</span></span>
* <span data-ttu-id="0699a-1645">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0699a-1646">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0699a-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0699a-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0699a-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0699a-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0699a-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0699a-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="0699a-1650">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1651">Az.Websites</span></span>
* <span data-ttu-id="0699a-1652">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0699a-1653">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0699a-1654">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0699a-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0699a-1655">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="0699a-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0699a-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1656">Az.Accounts</span></span>
* <span data-ttu-id="0699a-1657">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1658">Az.Compute</span></span>
* <span data-ttu-id="0699a-1659">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="0699a-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0699a-1660">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0699a-1661">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1663">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0699a-1664">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0699a-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0699a-1665">Az.EventGrid</span></span>
* <span data-ttu-id="0699a-1666">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0699a-1667">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0699a-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0699a-1668">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0699a-1669">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="0699a-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0699a-1670">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0699a-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0699a-1671">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0699a-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0699a-1672">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0699a-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0699a-1673">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="0699a-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0699a-1674">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0699a-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0699a-1675">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0699a-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="0699a-1676">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0699a-1677">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="0699a-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0699a-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0699a-1678">Az.IotHub</span></span>
* <span data-ttu-id="0699a-1679">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0699a-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0699a-1680">Az.LogicApp</span></span>
* <span data-ttu-id="0699a-1681">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="0699a-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1682">Az.Resources</span></span>
* <span data-ttu-id="0699a-1683">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0699a-1684">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0699a-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0699a-1685">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0699a-1686">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0699a-1687">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="0699a-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0699a-1688">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0699a-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0699a-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0699a-1689">Az.SignalR</span></span>
* <span data-ttu-id="0699a-1690">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1691">Az.Sql</span></span>
* <span data-ttu-id="0699a-1692">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0699a-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1693">Az.Storage</span></span>
* <span data-ttu-id="0699a-1694">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0699a-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0699a-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="0699a-1696">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="0699a-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0699a-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0699a-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1698">Az.Websites</span></span>
* <span data-ttu-id="0699a-1699">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0699a-1700">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0699a-1701">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0699a-1702">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-1702">General</span></span>

- <span data-ttu-id="0699a-1703">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="0699a-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="0699a-1704">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="0699a-1704">Online help for each module</span></span>
- <span data-ttu-id="0699a-1705">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="0699a-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0699a-1706">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0699a-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0699a-1707">Az.Accounts</span></span>
- <span data-ttu-id="0699a-1708">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0699a-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="0699a-1709">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="0699a-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0699a-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="0699a-1711">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="0699a-1711">Fixes for #7002</span></span>
- <span data-ttu-id="0699a-1712">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0699a-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0699a-1713">Az.Batch</span></span>
- <span data-ttu-id="0699a-1714">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0699a-1715">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="0699a-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0699a-1716">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0699a-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0699a-1717">Az.Billing</span></span>
- <span data-ttu-id="0699a-1718">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0699a-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="0699a-1720">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0699a-1721">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0699a-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="0699a-1723">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0699a-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0699a-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0699a-1725">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="0699a-1727">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0699a-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0699a-1728">Az.Monitor</span></span>
- <span data-ttu-id="0699a-1729">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0699a-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0699a-1730">Az.KeyVault</span></span>
- <span data-ttu-id="0699a-1731">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0699a-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0699a-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="0699a-1733">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="0699a-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0699a-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0699a-1734">Az.Media</span></span>
- <span data-ttu-id="0699a-1735">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="0699a-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0699a-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1736">Az.Network</span></span>
<span data-ttu-id="0699a-1737">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0699a-1738">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="0699a-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0699a-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0699a-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0699a-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0699a-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0699a-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0699a-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0699a-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0699a-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0699a-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0699a-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0699a-1747">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0699a-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0699a-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0699a-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0699a-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0699a-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0699a-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0699a-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0699a-1753">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0699a-1754">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0699a-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0699a-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0699a-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0699a-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0699a-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0699a-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0699a-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0699a-1758">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0699a-1759">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0699a-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="0699a-1761">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0699a-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0699a-1762">Az.Profile</span></span>
- <span data-ttu-id="0699a-1763">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="0699a-1765">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0699a-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1766">Az.Resources</span></span>
- <span data-ttu-id="0699a-1767">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0699a-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="0699a-1769">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="0699a-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0699a-1770">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0699a-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0699a-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="0699a-1772">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0699a-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0699a-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1773">Az.Sql</span></span>
- <span data-ttu-id="0699a-1774">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0699a-1775">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0699a-1776">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0699a-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1777">Az.Storage</span></span>
- <span data-ttu-id="0699a-1778">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0699a-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1779">Az.Websites</span></span>
- <span data-ttu-id="0699a-1780">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0699a-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0699a-1781">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0699a-1782">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-1782">General</span></span>

* <span data-ttu-id="0699a-1783">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="0699a-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0699a-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1784">Az.Compute</span></span>

* <span data-ttu-id="0699a-1785">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="0699a-1787">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0699a-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0699a-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="0699a-1789">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="0699a-1790">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0699a-1791">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0699a-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="0699a-1793">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0699a-1794">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="0699a-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0699a-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1795">Az.Resources</span></span>

* <span data-ttu-id="0699a-1796">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0699a-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0699a-1797">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0699a-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0699a-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1798">Az.Sql</span></span>

* <span data-ttu-id="0699a-1799">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="0699a-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0699a-1800">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0699a-1801">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0699a-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1802">Az.Storage</span></span>

* <span data-ttu-id="0699a-1803">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0699a-1804">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0699a-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0699a-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0699a-1806">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="0699a-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0699a-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0699a-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0699a-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0699a-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1809">Az.Websites</span></span>

* <span data-ttu-id="0699a-1810">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0699a-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0699a-1811">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0699a-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0699a-1812">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="0699a-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0699a-1813">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0699a-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0699a-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="0699a-1815">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0699a-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0699a-1816">Az.Automation</span></span>
* <span data-ttu-id="0699a-1817">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0699a-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0699a-1818">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0699a-1819">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0699a-1820">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0699a-1821">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0699a-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1822">Az.Compute</span></span>
* <span data-ttu-id="0699a-1823">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0699a-1824">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0699a-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="0699a-1826">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0699a-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0699a-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0699a-1828">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0699a-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1829">Az.Network</span></span>
* <span data-ttu-id="0699a-1830">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0699a-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0699a-1831">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0699a-1832">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0699a-1833">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0699a-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0699a-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0699a-1835">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0699a-1836">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="0699a-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0699a-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0699a-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0699a-1838">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="0699a-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0699a-1839">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0699a-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0699a-1840">Az.Relay</span></span>
* <span data-ttu-id="0699a-1841">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="0699a-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0699a-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1842">Az.Resources</span></span>
* <span data-ttu-id="0699a-1843">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0699a-1844">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="0699a-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0699a-1845">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0699a-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0699a-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-1847">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0699a-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1848">Az.Sql</span></span>
* <span data-ttu-id="0699a-1849">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0699a-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0699a-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0699a-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0699a-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0699a-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0699a-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0699a-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0699a-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0699a-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0699a-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0699a-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0699a-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0699a-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0699a-1858">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="0699a-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0699a-1859">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="0699a-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0699a-1860">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="0699a-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0699a-1861">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="0699a-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0699a-1862">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="0699a-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0699a-1863">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0699a-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0699a-1864">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0699a-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0699a-1865">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0699a-1866">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0699a-1867">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0699a-1867">General</span></span>
* <span data-ttu-id="0699a-1868">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="0699a-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0699a-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0699a-1869">Az.Profile</span></span>
* <span data-ttu-id="0699a-1870">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0699a-1871">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0699a-1872">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0699a-1873">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0699a-1874">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0699a-1875">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0699a-1876">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="0699a-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0699a-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="0699a-1878">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1879">Az.Compute</span></span>
* <span data-ttu-id="0699a-1880">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0699a-1881">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="0699a-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0699a-1882">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="0699a-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1884">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="0699a-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0699a-1885">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0699a-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0699a-1886">Az.Insights</span></span>
* <span data-ttu-id="0699a-1887">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="0699a-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0699a-1888">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="0699a-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0699a-1889">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0699a-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0699a-1890">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1891">Az.Network</span></span>
* <span data-ttu-id="0699a-1892">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0699a-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0699a-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0699a-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0699a-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0699a-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0699a-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0699a-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0699a-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0699a-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0699a-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0699a-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0699a-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0699a-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0699a-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0699a-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="0699a-1900">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1901">Az.Resources</span></span>
* <span data-ttu-id="0699a-1902">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0699a-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0699a-1903">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="0699a-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0699a-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0699a-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="0699a-1905">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="0699a-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0699a-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0699a-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="0699a-1907">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0699a-1908">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0699a-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0699a-1909">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="0699a-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0699a-1910">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="0699a-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0699a-1911">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0699a-1912">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0699a-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0699a-1913">Az.Profile</span></span>
* <span data-ttu-id="0699a-1914">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0699a-1915">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1916">Az.Compute</span></span>
* <span data-ttu-id="0699a-1917">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="0699a-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0699a-1918">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0699a-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0699a-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="0699a-1920">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0699a-1921">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0699a-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0699a-1922">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="0699a-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0699a-1923">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="0699a-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0699a-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0699a-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1925">Az.Network</span></span>
* <span data-ttu-id="0699a-1926">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="0699a-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0699a-1927">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1928">Az.Resources</span></span>
* <span data-ttu-id="0699a-1929">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0699a-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0699a-1930">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0699a-1931">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0699a-1932">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0699a-1932">Azure.Storage</span></span>
* <span data-ttu-id="0699a-1933">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="0699a-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0699a-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0699a-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0699a-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0699a-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0699a-1936">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="0699a-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0699a-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0699a-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0699a-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0699a-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="0699a-1939">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0699a-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0699a-1940">Az.Compute</span></span>
* <span data-ttu-id="0699a-1941">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="0699a-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0699a-1942">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0699a-1943">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="0699a-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0699a-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0699a-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0699a-1945">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0699a-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0699a-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0699a-1946">Az.Network</span></span>
* <span data-ttu-id="0699a-1947">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0699a-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0699a-1948">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1948">new cmdlets added</span></span>
    - <span data-ttu-id="0699a-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0699a-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0699a-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0699a-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0699a-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0699a-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0699a-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0699a-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0699a-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0699a-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0699a-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0699a-1955">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0699a-1956">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0699a-1957">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0699a-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0699a-1958">Az.RedisCache</span></span>
* <span data-ttu-id="0699a-1959">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="0699a-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0699a-1960">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0699a-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0699a-1961">Az.Resources</span></span>
* <span data-ttu-id="0699a-1962">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0699a-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0699a-1963">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="0699a-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0699a-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0699a-1964">Az.Sql</span></span>
* <span data-ttu-id="0699a-1965">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="0699a-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0699a-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0699a-1966">Az.Websites</span></span>
* <span data-ttu-id="0699a-1967">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="0699a-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0699a-1968">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="0699a-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0699a-1969">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="0699a-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0699a-1970">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="0699a-1970">Initial Release</span></span>
